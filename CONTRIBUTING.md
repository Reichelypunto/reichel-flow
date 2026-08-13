# Contribuir a REICHEL FLOW

REICHEL FLOW está en fase de definición técnica. Toda contribución debe partir de un issue o brief aprobado y respetar las fuentes de verdad descritas en `README.md` y `AGENTS.md`.

## Antes de empezar

- Confirma alcance, criterios de aceptación y dependencias.
- Revisa `docs/architecture/`, `docs/decisions/` y `docs/development/`.
- No elijas stack, framework o proveedor sin una decisión aprobada.
- No desarrolles funciones anticipadas ni añadas dependencias preventivas.

## Flujo

Usa el proceso definido en [docs/development/workflow.md](docs/development/workflow.md). Cada rama y PR debe cubrir un objetivo coherente y trazable al issue o brief.

## Calidad de la contribución

- Mantén los cambios pequeños, comprensibles y dentro del alcance.
- Añade pruebas para el comportamiento que cambie cuando ya exista código ejecutable.
- Actualiza la documentación técnica afectada.
- Explica decisiones y trade-offs relevantes.
- No acoples el core a WhatsApp, Chrome, una plataforma cliente o un proveedor de IA.
- Mantén control humano en acciones sensibles.

## Commits y pull requests

Usa mensajes de commit breves y descriptivos. La PR debe indicar:

- issue o brief relacionado;
- qué cambia y por qué;
- cómo se verificó;
- riesgos y límites conocidos;
- decisiones pendientes.

La revisión y el merge son obligatorios salvo una excepción explícita de la persona responsable del repositorio.

## Seguridad

No publiques secretos ni datos sensibles. Los ejemplos deben usar valores ficticios. Si una tarea requiere credenciales, utiliza el mecanismo seguro aprobado para el entorno y documenta únicamente el nombre de la configuración, nunca su valor.
