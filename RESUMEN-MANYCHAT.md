# Resumen: skill para crear flujos de ManyChat

Resumen de la conversación para continuarla en otro sitio. Solo recoge lo que se habló o se encontró en la sesión. Lo que no recuerdo con seguridad lo marco como "no lo recuerdo".

Las búsquedas se hicieron el 2026-10-21. Las fechas de actualización y las estrellas son las que devolvió GitHub ese día y pueden haber cambiado.

## 1. Qué se pidió

Petición literal: "Usa /findskills para encontrar alguna skill que cree flujos de Manychat".

- `/findskills` no estaba entre las skills disponibles. Para buscar usé `SearchSkills`, `SearchPlugins`, `SearchMcpRegistry`, el repo local y GitHub.
- Después se pidió buscar también en GitHub ("Has buscado en GitHub?" y "Sí, busca en todo GitHub").
- Más tarde se planteó crear una skill propia partiendo de las existentes y adaptándola a lo que la usuaria suele hacer.
- La parte de "venderlo" **no consta** en esta conversación. No lo recuerdo como petición de la usuaria.
- La frase "con buena calificación" tampoco consta con esas palabras. Lo más parecido son las estrellas de los repos.

## 2. Qué se encontró

### Dentro de Claude (skills, plugins y conectores)

No apareció nada de ManyChat. Lo más cercano, y ninguno crea flujos de ManyChat:

- Plugin **MyChatBot**: crea agentes de ventas con IA en su propia plataforma. Publicado en el directorio de plugins de Anthropic.
- Plugin **Voicenter Bot Builder**: genera JSON de bots de Voicenter. Su método de especificación, detalle y ensamblado podría servir de inspiración.
- Conector **Mermaid Chart**: solo dibuja diagramas.

Tampoco hay ManyChat en el repo `reichelypunto/reichel-flow`: la búsqueda local no dio resultados. La búsqueda de código de GitHub dio 0 resultados, pero marcó `incomplete_results: true`.

### GitHub público

Datos de la búsqueda de repositorios. "Abierto" quiere decir que leí su contenido.

**Skills que construyen o escriben flujos**

| Repo | Qué hace | Estrellas | Últ. actualización | ¿Abierto? |
|---|---|---|---|---|
| [danilf-hash/manychat-builder-skill](https://github.com/danilf-hash/manychat-builder-skill) | Construye embudos de DM de Instagram manejando el navegador (Claude Code + MCP de Chrome). Es un README de instrucciones en ruso. | 0 | 2026-03-31 | Sí |
| [kingsleylow123/manychat-comment-dm](https://github.com/kingsleylow123/manychat-comment-dm) | Automatización "comentario a DM" con comprobación de seguimiento, manejando Chrome. | 0 | 2026-10-02 | Sí |
| [paulovyn1/manychat-flow-writer](https://github.com/paulovyn1/manychat-flow-writer) | Skill para redactar flujos. Solo vi la descripción ("Skill ManyChat Flow Writer — Triwer"). | 0 | 2026-06-17 | No |
| [jetsuthpring/cta-writer](https://github.com/jetsuthpring/cta-writer) | Convierte guiones cortos en configuraciones de comentario a DM hacia vídeos de YouTube. | 0 | 2026-05-02 | No |
| [JHamidun/claude-code-config-pack](https://github.com/JHamidun/claude-code-config-pack) | Paquete de configuración que incluye la skill `manychat-funnel-ru` (en ruso). | No lo recuerdo | No lo recuerdo | No (solo el fragmento de la búsqueda) |
| [wubin1836/ai-hive-agent-skills](https://github.com/wubin1836/ai-hive-agent-skills) | Skills de otro producto (AI-HIVE) que generan reglas, respuestas y pruebas de flujo. No son una integración con ManyChat. | No lo recuerdo | No lo recuerdo | No (solo el fragmento de la búsqueda) |

**Servidores MCP para la API de ManyChat**

Gestionan suscriptores, etiquetas, campos y envío de flujos ya existentes. Ninguno crea flujos.

| Repo | Estrellas | Últ. actualización | ¿Abierto? |
|---|---|---|---|
| [WIZNEOAI/Manychat-MCP](https://github.com/WIZNEOAI/Manychat-MCP) (CLI + MCP en TypeScript, comprueba reglas de Meta antes de enviar, 4 issues abiertos) | 0 | 2026-09-21 | No |
| [AleemHaider/manychat-mcp](https://github.com/AleemHaider/manychat-mcp) (Python) | 1 | 2026-06-24 | No |
| [fabienbutz/manychat-mcp](https://github.com/fabienbutz/manychat-mcp) (TypeScript) | 0 | 2026-04-21 | No |

Otros resultados que aparecieron y no usé: `francesca-tabor-ai/keyword-automation` (2 estrellas, "sistema estilo ManyChat con Claude Code y MCP"), `ojuliocouto/skill-criador-dash` (2 estrellas, dashboards de marketing que mencionan ManyChat) y varios repos de webhooks entre ManyChat y la API de Claude. No los abrí.

### Por qué sí o por qué no sirven (solo los dos que abrí)

- **manychat-comment-dm (Kingsley):**
  - Sirve como base: pide los datos primero con valores por defecto y comprueba que no choquen palabras clave.
  - Incluye pasos previos de Instagram, una prueba final con segunda cuenta y soluciones para problemas conocidos.
  - Solo cubre un tipo de flujo.
  - Su texto afirma que la API pública de ManyChat no puede crear flujos, disparadores ni esperas.
- **manychat-builder-skill (Danil):**
  - Sirve como guía de la interfaz de ManyChat, con tres patrones de embudo y trucos para escribir texto.
  - No tiene proceso ni comprobaciones, y está en ruso.
  - Indica que Condition, Randomizer y Smart Delay requieren plan PRO (o prueba de 14 días), y que hay un límite de 3 botones por mensaje y de 1000 caracteres por texto.
- Ninguno de los dos repos tiene un solo uso o estrella visible (0 estrellas, 0 forks). No encontré contenido sospechoso: son archivos de texto de instrucciones, sin scripts ni dependencias. El único fragmento de código es un parche de `fetch` por si el lienzo no carga.

## 3. Conclusión

- **No hay nada con buena calificación.** Las mejores candidatas tienen 0 estrellas. Lo que existe son proyectos pequeños de particulares.
- Hay dos bases útiles para partir de ellas (las dos que abrí).
- La usuaria propuso crear una skill propia partiendo de esas bases y de lo que ella suele hacer. Quedó como dirección probable, no como decisión cerrada.

## 4. Plan propuesto

**Método:** la API de ManyChat no permite crear flujos (según la skill de Kingsley; no lo comprobé en la documentación oficial) y no hay MCP oficial. Por eso la skill trabajaría con **Claude in Chrome**: Claude maneja el editor visual de ManyChat en el Chrome de la usuaria. Esto es fiable solo mientras ManyChat no cambie su interfaz.

**Pasos propuestos:**
1. Comprobar que Claude in Chrome está instalado y que ve ManyChat.
2. Leer las skills de email de la usuaria (`keles-reichel-email`, `name-reichel-email`, `qa-mensual-email-whatsapp`) para reutilizar lo que ya funciona. No las he abierto.
3. Recoger lo que la usuaria suele hacer: qué flujos monta más, su tono y plantillas, y algún flujo de ejemplo.
4. Escribir la skill partiendo de la estructura de Kingsley: pedir datos, comprobar condiciones previas, montar, revisar y probar.
5. Mejoras propuestas sobre las bases:
   - biblioteca de varios patrones de flujo (lead magnet, calificación con botones, secuencia con esperas);
   - textos y tono propios;
   - paso de revisión humana antes de dejar el flujo activo;
   - modo "solo diseño" que entregue texto y diagrama, para usarlo sin Chrome o desde el móvil;
   - comprobaciones de destinos de botones, límites de texto y configuración de Instagram.

**Qué haría falta:**
- Ordenador con Chrome y la extensión Claude in Chrome.
- Cuenta de ManyChat con la sesión iniciada. Para condiciones y esperas, plan PRO o prueba de 14 días (según el README de Danil).
- Instagram profesional conectado a ManyChat y activada la opción "Permitir acceso a los mensajes" (según la skill de Kingsley).
- Claves de API: **ninguna** para el método de navegador. Solo harían falta si se quisiera usar un MCP de la API.
- Nunca se escriben contraseñas ni códigos de verificación: si hay que iniciar sesión, lo hace la usuaria.

**Aclaraciones de la conversación:**
- "BA" es Builderall. La usuaria dijo que comparaba esto con lo que se hace allí con mails, y que se refería a que Claude puede actuar en una web mediante el navegador sin MCP ni API. No sé cómo se hacen exactamente los mails en Builderall.
- Se habló de un "modo de aprendizaje" y propuse tres interpretaciones (estilo de salida "learning" de Claude Code, que Claude aprenda viéndola montar un flujo, o hacerlo paso a paso a mano). **La usuaria no eligió ninguna.**

## 5. Qué hay en este ordenador

- **Archivo creado:** `/home/user/reichel-flow/RESUMEN-MANYCHAT.md` (este, sin añadir a git ni commitear).
- **Repos clonados, solo lectura y sin instalar:**
  - `/home/user/danilf-hash/manychat-builder-skill` (un `README.md`)
  - `/home/user/kingsleylow123/manychat-comment-dm` (un `README.md` y `skills/manychat-comment-dm/SKILL.md`)
  - Están fuera de `reichel-flow` y los clonó el comando de lectura que dio el sistema (`--depth 1`).
- No he instalado skills, plugins ni conectores. No he modificado ni borrado ningún otro archivo de `reichel-flow`. No he usado el directorio temporal de la sesión para nada.

## 6. Pendiente o sin decidir

- Comprobar Claude in Chrome en el ordenador (primer paso del plan).
- Elegir el "modo de aprendizaje" (las tres opciones).
- Qué flujos monta más la usuaria, su tono y algún ejemplo.
- Si la skill construye en el navegador o solo entrega el diseño (o ambas cosas, que fue lo que propuse).
- Dónde se guarda la skill. Propuse una carpeta fuera de `reichel-flow`; la decisión es suya. El `AGENTS.md` exige aprobación explícita para añadir dependencias o proveedores y limita el alcance a trabajo aprobado.
- Abrir las otras candidatas (`manychat-flow-writer`, `cta-writer`, `manychat-funnel-ru`, los MCP) si se quiere comparar.
- Si el objetivo es vender la skill: **no consta en la conversación**. No se habló de precio, canal ni modelo de negocio.
- Si el objetivo es para REICHEL FLOW o solo una herramienta de contenido: lo pregunté y no se contestó.
