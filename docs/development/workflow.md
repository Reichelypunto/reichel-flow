# Workflow técnico

El flujo estándar es:

`Issue/Brief → rama → implementación → tests → PR → revisión → merge`

## 1. Issue o brief

Debe definir problema, alcance, fuera de alcance, criterios de aceptación, fuentes funcionales y decisiones pendientes. Si el trabajo exige una decisión no aprobada, primero se compara y documenta; no se elige arbitrariamente.

## 2. Rama

Crea una rama desde `main` actualizada. Usa un nombre trazable y corto, por ejemplo `rf-001-evaluar-stack`. No mezcles objetivos independientes.

## 3. Implementación

Implementa solo el alcance aprobado. Mantén límites de adaptación y evita nuevas dependencias o abstracciones no justificadas. Actualiza la documentación técnica afectada.

## 4. Tests

Ejecuta las comprobaciones proporcionales al cambio. Cuando exista código, incluye pruebas automatizadas del comportamiento nuevo o modificado. Registra comandos, resultados y limitaciones; no declares una prueba como superada si no se ejecutó.

## 5. Pull request

La PR debe enlazar el issue o brief e incluir resumen, motivación, verificación, riesgos, decisiones y trabajo excluido. Debe ser lo bastante pequeña para revisarse con claridad.

## 6. Revisión

La revisión comprueba alcance, criterios de aceptación, arquitectura, seguridad, pruebas y documentación. Los comentarios sustanciales se resuelven o se documenta explícitamente por qué no aplican.

## 7. Merge

Se fusiona solo con aprobación y comprobaciones requeridas correctas. Después del merge, confirma el estado de `main`, cierra o actualiza el issue y registra cualquier decisión aprobada o seguimiento necesario.

## Excepciones

Solo la persona responsable del repositorio puede autorizar una excepción. Debe quedar registrada con su motivo y alcance; una urgencia no autoriza a publicar secretos, omitir control humano ni acoplar el core a un proveedor.
