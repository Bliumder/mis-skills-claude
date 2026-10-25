# Guía de uso

## 1. Instalar todo en tu ordenador (una sola vez)

Abre Claude Code en cualquier carpeta y pega este prompt:

```text
Instala mis plugins de Claude Code a nivel de usuario. Ejecuta estos comandos uno por uno
con la CLI `claude` y dime si alguno falla:

claude plugin marketplace add Bliumder/mis-skills-claude
claude plugin install emil-skills@mis-skills-claude
claude plugin install scroll-world@mis-skills-claude
claude plugin install taste-skill@mis-skills-claude
claude plugin install ui-ux-pro-max@mis-skills-claude
claude plugin install react-native-skills@mis-skills-claude
claude plugin install impeccable@mis-skills-claude
claude plugin install marketing-skills@mis-skills-claude
claude plugin install task-observer@mis-skills-claude
claude plugin install archify@mis-skills-claude

claude plugin marketplace add thedotmack/claude-mem
claude plugin install claude-mem@thedotmack
npx claude-mem install

Después:
1. Ejecuta `claude plugin list` y muéstrame que los 10 plugins están activados.
2. Comprueba que tengo instalados node (18 o superior), python3 y Chrome/Chromium,
   y dime cuál falta.
3. Añade a ~/.claude/settings.json, dentro de "env", "DO_NOT_TRACK": "1" para
   desactivar la telemetría de impeccable y claude-mem (sin borrar lo que ya haya).
4. Recuérdame reiniciar Claude Code.
```

Para actualizar más adelante: `claude plugin marketplace update mis-skills-claude`.

## 2. Usarlas en un proyecto (y en sesiones en la nube)

Las sesiones de Claude Code en la nube (claude.ai/code) empiezan con un contenedor limpio,
así que ahí no sirve instalarlos "en tu ordenador". Lo que sí funciona es declararlos
**dentro del repositorio**: copia [`plantillas/settings.json`](plantillas/settings.json) a
`.claude/settings.json` de tu proyecto y haz commit. Claude Code ofrecerá instalar los
plugins al abrir el proyecto, en local o en la nube.

> En la nube, la red del entorno debe permitir `github.com` (y npm para claude-mem).

## 3. Que trabajen juntas sin pisarse

Se activan solas según lo que pidas, pero varias se solapan (sobre todo las de diseño).
Copia [`plantillas/CLAUDE.md`](plantillas/CLAUDE.md) a la raíz de tu proyecto (o a
`~/.claude/CLAUDE.md` para todos tus proyectos) y ajústalo: le dice a Claude cuál usar
en cada caso y en qué orden.

También puedes llamarlas a mano escribiendo `/` y el nombre, por ejemplo:

| Quiero… | Escribe |
|---|---|
| Dirección de arte para una landing | `/design-taste-frontend` |
| Pulir o auditar una interfaz | `/impeccable polish` · `/impeccable audit` |
| Paleta, tipografía o estilo para mi stack | `/ui-ux-pro-max:ui-ux-pro-max` |
| Animar algo | `/emil-skills:animate` |
| Revisar animaciones | `/emil-skills:review-animations` |
| Romper un componente con datos extremos | `/emil-skills:break-ui` |
| Landing con scroll cinemático 3D | `/scroll-world` |
| App React Native / Expo | `/react-native-skills:vercel-react-native-skills` |
| Diagrama de arquitectura, ERD, secuencia… | `/archify` |
| Copy de una web | `/marketing-skills:copywriting` |
| Mejorar conversión de una página | `/marketing-skills:cro` |
| Plan de marketing completo | `/marketing-skills:marketing-plan` |
| Buscar en lo que hice en sesiones anteriores | `/claude-mem:mem-search` |
| Revisión semanal de mejoras a mis skills | `/task-observer` |

## 4. ¿Y en los chats normales de claude.ai?

Los plugins son de **Claude Code** (terminal, app de escritorio, web claude.ai/code e IDE).
Los chats normales de claude.ai no instalan plugins: allí solo puedes subir skills sueltas
como .zip desde los ajustes de Capacidades/Skills, si tu plan lo permite. Las que mejor
funcionan así son las que solo tienen Markdown (emil-skills, react-native-skills,
marketing-skills sin sus CLIs, task-observer). Las que necesitan Node, Chrome, hooks o
servicios en segundo plano (impeccable, claude-mem, archify, taste-skill, scroll-world)
úsalas en Claude Code.
