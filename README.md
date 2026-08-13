# REICHEL FLOW

REICHEL FLOW será un sistema operativo de comunidades y automatización conversacional. Su objetivo es automatizar trabajo, no limitarse al envío de mensajes.

Este repositorio es la fuente de verdad del código y de la documentación técnica. El producto todavía está en fase de definición: aquí no hay código de aplicación, un framework elegido ni infraestructura configurada.

## Límites actuales

- WhatsApp será el primer conector, no el núcleo del producto.
- Chrome, las aplicaciones de escritorio o móviles y los proveedores de IA son adaptadores sustituibles.
- La complejidad debe quedar en el motor, no trasladarse a la usuaria.
- Las acciones sensibles deben conservar control humano.
- Ningún proveedor de IA puede convertirse en un punto único de fallo.
- La arquitectura y el stack del MVP se decidirán mediante un proceso comparativo documentado.

## Fuentes de verdad

| Contenido | Fuente |
| --- | --- |
| Código y documentación técnica | Este repositorio de GitHub |
| Producto, Blueprint y documentación funcional | Google Drive, carpeta `INFRAESTRUCTURA REICHEL/01. Proyectos/REICHEL FLOW` |
| Tareas, prioridades e ideas | Notion |

No se debe duplicar en GitHub toda la documentación funcional de Drive. Este repositorio conserva solo el contexto necesario para tomar e implementar decisiones técnicas.

## Documentación técnica

- [Reglas para agentes](AGENTS.md)
- [Cómo contribuir](CONTRIBUTING.md)
- [Arquitectura](docs/architecture/README.md)
- [Principios de arquitectura](docs/architecture/principles.md)
- [Decisiones técnicas](docs/decisions/README.md)
- [Desarrollo](docs/development/README.md)
- [Workflow técnico](docs/development/workflow.md)

## Estado

Base documental técnica inicial. No iniciar el desarrollo del producto hasta que exista un brief o issue aprobado y se hayan resuelto las decisiones técnicas necesarias.
