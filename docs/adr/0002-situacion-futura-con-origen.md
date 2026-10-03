# La Situación futura se clona de la actual conservando el Origen de cada elemento

Al crear la Situación futura de un Canvas se clona la Situación actual y cada elemento clonado guarda una referencia (Origen) al elemento del que procede. Así la Transición (cambios de dueño, evolución de Componentes, Blockers resueltos) se calcula comparando las dos Situaciones.

## Considered Options

- **Dos copias independientes**: lo más simple, pero se pierde qué cambió, y "facilitar la transición" es un objetivo del producto.
- **Un solo modelo con estado por elemento (actual/futuro/ambos)**: no duplica datos, pero se complica en cuanto un atributo difiere entre situaciones (dueño, evolución, tipo de equipo), que es justo el caso habitual.
- **Clonar con Origen** (elegida): cada Situación es un modelo completo y editable por sí mismo, y la Transición es una diferencia calculable.
