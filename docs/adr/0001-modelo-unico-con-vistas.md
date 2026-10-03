# Un único modelo de dominio con tres vistas, no tres diagramas independientes

Wardley Map, Context Map y Team Topology se tratan como Vistas de un mismo modelo por Canvas, no como tres diagramas con datos propios. El mismo elemento (p. ej. una capacidad del Wardley Map) se clasifica como subdominio, se agrupa en un Bounded Context y tiene un equipo propietario sin duplicarse entre diagramas.

## Considered Options

- **Tres diagramas independientes con vínculos opcionales**: más barato de construir y cada editor evoluciona aislado, pero la coherencia entre estrategia, software y organización (la propuesta de valor central) recae en el usuario, y añadir un modelo compartido después equivale a reescribir los editores y migrar datos.
- **Modelo único con vistas** (elegida): más coste inicial y los editores dejan de ser independientes, pero la integración semántica y las sugerencias entre perspectivas salen del propio modelo.

## Consequences

La vinculación componente ↔ Bounded Context ↔ equipo deja de ser un should-have post-MVP (PRD §6.2): un mínimo de vínculos forma parte del MVP.
