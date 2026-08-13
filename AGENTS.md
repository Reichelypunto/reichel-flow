# AGENTS.md

## Qué es REICHEL FLOW

REICHEL FLOW será un sistema operativo de comunidades y automatización conversacional. Automatiza trabajo, no solo mensajes. WhatsApp es el primer conector previsto, pero el producto no depende de WhatsApp, WaToolbox, Chrome ni de un proveedor concreto de IA.

## Fuentes de verdad

- **GitHub:** código y documentación técnica.
- **Google Drive:** producto, Blueprint, flujos confirmados y documentación funcional. Carpeta: `INFRAESTRUCTURA REICHEL/01. Proyectos/REICHEL FLOW`.
- **Notion:** tareas, prioridades e ideas.

No copies a GitHub toda la documentación funcional de Drive. Trae únicamente el contexto técnico imprescindible y enlaza o identifica la fuente cuando corresponda. El historial de chats no es una fuente de verdad.

## Antes de trabajar

1. Lee `README.md`, este archivo y la documentación relevante dentro de `docs/`.
2. Lee el issue o brief asignado completo y confirma sus criterios de aceptación.
3. Consulta en Drive el contexto funcional necesario y en Notion la prioridad vigente, si tienes acceso.
4. Revisa las decisiones registradas y el estado actual del repositorio.
5. Si falta acceso o existe una contradicción que cambia el alcance, detente y solicita aclaración.

## Decisiones que no puedes tomar por tu cuenta

No elijas ni cambies sin aprobación explícita:

- framework, lenguaje, base de datos o stack del MVP;
- proveedor o servicio de infraestructura, IA o mensajería;
- arquitectura del núcleo o límites entre dominios;
- requisitos funcionales, prioridades o alcance;
- comportamiento de acciones sensibles o nivel de control humano;
- una integración que convierta WhatsApp, Chrome o un proveedor de IA en el núcleo;
- configuración de Cloudflare o despliegues de producción.

Cuando haya alternativas, documenta opciones, criterios, riesgos y recomendación; no conviertas una preferencia en una decisión aprobada.

## Reglas de implementación

- Trabaja solo sobre un issue o brief aprobado.
- No amplíes el alcance ni aproveches una tarea para añadir abstracciones, dependencias o funciones no solicitadas.
- Mantén WhatsApp, Chrome, escritorio, móvil y proveedores de IA detrás de límites de adaptación sustituibles.
- El core debe expresar capacidades del producto sin depender de APIs o modelos concretos.
- Las acciones sensibles requieren mecanismos explícitos de revisión, confirmación o intervención humana.
- No añadas boilerplate ni dependencias sin necesidad demostrable.
- Añade o actualiza pruebas y documentación en proporción al cambio.

## Secretos y datos sensibles

Nunca incluyas credenciales, tokens, claves, cookies, datos personales ni secretos en código, commits, issues, PR, logs, ejemplos o documentación. Usa nombres de variables y valores ficticios seguros. Si detectas un secreto, no lo reproduzcas: detén el trabajo, avisa y sigue el procedimiento de revocación/rotación que indique la persona responsable.

## Conflictos y ambigüedades

1. No resuelvas silenciosamente contradicciones entre GitHub, Drive, Notion o el brief.
2. Identifica las fuentes en conflicto y el impacto técnico.
3. Conserva el alcance aprobado y evita cambios irreversibles.
4. Solicita una decisión a la persona responsable.
5. Registra la resolución técnica aprobada en `docs/decisions/` cuando proceda.

La fuente competente depende del tema: GitHub para lo técnico, Drive para producto y función, Notion para prioridad. Un issue no puede modificar por sí solo una decisión explícita de producto sin aprobación.

## Entrega

Sigue `docs/development/workflow.md`:

`Issue/Brief → rama → implementación → tests → PR → revisión → merge`

La entrega debe incluir alcance realizado, archivos relevantes, pruebas ejecutadas, decisiones o supuestos, riesgos, bloqueos y siguiente paso. No declares terminado lo que no se haya verificado. No mezcles cambios ajenos ni incluyas secretos.
