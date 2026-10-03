# FlowCanvas

Herramienta para aplicar Architecture for Flow (Wardley Maps + DDD estratégico + Team Topologies) sobre un único modelo del sistema y su organización, guiando al usuario por los pasos del Architecture for Flow Canvas.

## Language

### Estructura

**Proyecto**:
El sistema u organización que se está modelando (p. ej. "Online School"). Agrupa uno o varios Canvas.
_Avoid_: Workspace, board

**Canvas**:
Una pasada completa por los Pasos de Architecture for Flow sobre un Proyecto, con su Situación actual y su Situación futura. Repetir el ejercicio meses después es un Canvas nuevo dentro del mismo Proyecto.
_Avoid_: Sesión, diagrama, mapa (como sinónimo de Canvas)

**Situación actual**:
El modelo del sistema y la organización tal como son hoy (as-is). Puede contener estados disfuncionales; están permitidos y se señalan.
_Avoid_: Estado actual, baseline

**Situación futura**:
El modelo objetivo (to-be), creado a partir de la Situación actual. Cada elemento conserva su Origen.
_Avoid_: Estado futuro, target

**Origen**:
La referencia de un elemento de la Situación futura al elemento de la Situación actual del que procede. Un elemento sin Origen es nuevo; un elemento actual sin descendiente queda retirado.
_Avoid_: Linaje, parent

**Transición**:
El conjunto de diferencias entre la Situación actual y la futura (cambios de dueño, evolución, equipos nuevos o retirados, Blockers resueltos).
_Avoid_: Roadmap, plan de migración

**Vista**:
Una proyección del modelo de una Situación en una notación concreta: Wardley Map, Context Map o Team Topology. Las Vistas no tienen datos propios; editar en una Vista edita el modelo compartido.
_Avoid_: Diagrama, editor (como entidad), pizarra

**Paso**:
Una de las etapas sugeridas del Canvas (equipos actuales, flow de cambio, usuarios y necesidades, landscape actual, problem space, solution space, landscape futuro, organización futura). Los Pasos guían, nunca bloquean.
_Avoid_: Fase, etapa, wizard step

### Estrategia (Wardley)

**Usuario**:
El anchor de la cadena de valor: quien tiene las Necesidades que el sistema satisface.
_Avoid_: Anchor (en la interfaz), actor, cliente

**Necesidad**:
Lo que un Usuario quiere conseguir; el primer nivel de la cadena de valor bajo el Usuario.
_Avoid_: Requisito, user need (mezclado)

**Componente**:
Un elemento de la cadena de valor con una posición de visibilidad y de evolución (Genesis, Custom, Product, Commodity). Se descompone en otros Componentes mediante dependencias.
_Avoid_: Nodo, capability (como sinónimo genérico)

**Subdominio**:
La clasificación Core, Supporting o Generic de un Componente que representa una capacidad de negocio. No es una entidad propia: no todos los Componentes tienen Subdominio.
_Avoid_: Dominio (a secas), área

### Solución y organización

**Bounded Context**:
Un límite de modelo de software que realiza uno o más Componentes y tiene exactamente un Equipo dueño en el caso ideal.
_Avoid_: Servicio, módulo, microservicio

**Equipo**:
Un equipo con un tipo de Team Topologies (Stream-aligned, Platform, Enabling, Complicated-subsystem o Undefined) que posee Bounded Contexts.
_Avoid_: Squad, grupo

**Interacción**:
La relación de trabajo entre dos Equipos, con un modo de Team Topologies (Collaboration, X-as-a-Service, Facilitation) o sin modo. Una Interacción sin modo es válida en la Situación actual y genera una Señal en la futura.
_Avoid_: Dependencia (entre equipos), comunicación

**Relación**:
El patrón de integración entre dos Bounded Contexts (Partnership, Shared Kernel, Customer-Supplier, Conformist, Anticorruption Layer, Open Host Service, Published Language, Separate Ways).
_Avoid_: Integración, conexión, Interacción (reservada a Equipos)

**Señal**:
Un aviso que el modelo genera por reglas cuando detecta un estado contrario a Architecture for Flow (p. ej. un Bounded Context con varios Equipos dueños, un Core en Commodity). Es la base de las sugerencias y de la educación contextual.
_Avoid_: Error, validación, warning, sugerencia IA

**Blocker**:
Un impedimento al flow de cambio, de un tipo del catálogo (dependencia entre equipos, hand-off, sobrecarga cognitiva, etc.), anclado a un Equipo, una interacción o un Componente. Un Blocker actual puede quedar resuelto en la Situación futura.
_Avoid_: Problema, issue, pain point

### Colaboración y arranque

**Comentario**:
Una conversación anclada a un elemento del modelo; se ve desde todas las Vistas donde aparece ese elemento.
_Avoid_: Nota (son cosas distintas)

**Nota**:
Texto libre colocado en una Vista, fuera del modelo, para trabajo de workshop. Puede promoverse a elemento del modelo.
_Avoid_: Sticky, post-it, Comentario

**Plantilla**:
Un Canvas de ejemplo con Situación actual y futura completas que se clona para empezar un Proyecto nuevo.
_Avoid_: Ejemplo, template de diagrama

**Rol**:
El permiso de una persona sobre un Proyecto: Propietario, Editor o Lector.
_Avoid_: Viewer/Editor (en inglés), permiso

**Enlace de lectura**:
Una URL revocable que permite ver un Canvas sin cuenta, pensada para asistentes de un workshop.
_Avoid_: Enlace público, share link
