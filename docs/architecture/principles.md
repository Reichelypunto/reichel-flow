# Principios de arquitectura

## 1. Automatizar trabajo

El sistema debe orquestar acciones y estados operativos, no limitarse al envío de mensajes.

## 2. Core independiente de canales

WhatsApp será el primer conector. WhatsApp, WaToolbox, Chrome y cualquier otro canal o superficie son adaptadores reemplazables, no el modelo central del producto.

## 3. Complejidad interna, experiencia simple

El motor absorbe la complejidad técnica. La experiencia no debe obligar a la usuaria a reproducir estructuras internas como “plantilla → workflow → selección de plantilla”. Un contenido creado dentro de una automatización puede convertirse internamente en un recurso reutilizable.

## 4. Recursos lógicos sustituibles

Los flujos deben poder referenciar recursos por su función para sustituirlos una vez sin reconstruir automatizaciones relacionadas.

## 5. Operación fiable y observable

Las operaciones prolongadas necesitan estado persistente, historial y controles coherentes como pausa, reanudación, cancelación y reintento. Los detalles se definirán en decisiones posteriores.

## 6. Control humano en acciones sensibles

La automatización no elimina la supervisión. Las acciones con impacto sensible deben incorporar confirmación, revisión o intervención humana. El sistema nunca debe eliminar automáticamente un contacto.

## 7. Proveedores sustituibles

Ningún proveedor de IA, mensajería, almacenamiento o infraestructura debe ser un punto único de fallo por diseño. Las capacidades se expresan mediante contratos propios y límites claros.

## 8. Seguridad y privacidad desde el diseño

Aplicar mínimo privilegio, separación de secretos, trazabilidad y minimización de datos. Los secretos nunca forman parte del repositorio.

## 9. Evolución multiplataforma

Las decisiones deben considerar WhatsApp Web y Chrome sin impedir una aplicación de escritorio, acceso móvil u otros canales futuros.

## 10. Centro de operaciones

La experiencia principal futura será un centro de operaciones que priorice trabajo y estado, no un menú que exponga la estructura técnica de módulos.

## 11. Decisiones trazables y reversibles

Las decisiones relevantes se comparan, aprueban y registran. Se favorecen límites que reduzcan el coste de sustituir tecnologías o proveedores.

## 12. Entrega guiada por alcance

Cada cambio responde a un issue o brief aprobado. No se anticipan funciones, infraestructura ni abstracciones sin necesidad validada.
