# Arquitectura

Este directorio contendrá la descripción técnica de REICHEL FLOW: límites del sistema, componentes, contratos, flujos técnicos y atributos de calidad.

## Estado actual

La arquitectura y el stack del MVP no están decididos. No existe todavía código de aplicación ni configuración de infraestructura. La primera decisión deberá comparar alternativas usando criterios explícitos antes de recomendar una dirección.

## Orientación inicial

La arquitectura deberá separar, como mínimo, conceptos de negocio, orquestación, persistencia e integraciones. Esta orientación no fija todavía módulos, procesos, repositorios, frameworks ni tecnologías.

Los siguientes elementos son adaptadores y no deben definir el core:

- WhatsApp y otros canales de conversación;
- Chrome y otras superficies cliente;
- aplicaciones de escritorio o móviles;
- proveedores de IA;
- proveedores de almacenamiento o infraestructura.

Las capacidades confirmadas del producto deben validarse contra el Blueprint de Drive cuando una decisión técnica las necesite. No se duplicará aquí la especificación funcional completa.

## Contenido futuro

Cuando las decisiones sean aprobadas, este directorio podrá incorporar diagramas, límites de contexto, contratos, modelos de datos y estrategias de despliegue. Toda decisión relevante debe quedar registrada en `docs/decisions/`.

Consulta también [principles.md](principles.md).
