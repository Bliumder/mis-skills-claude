# mis-skills-claude

Marketplace personal de plugins para Claude Code.

## Instalación

```
/plugin marketplace add Bliumder/mis-skills-claude
/plugin install <plugin>@mis-skills-claude
```

## Plugins

Instalar cada plugin:

```
/plugin install emil-skills@mis-skills-claude
/plugin install scroll-world@mis-skills-claude
/plugin install taste-skill@mis-skills-claude
/plugin install ui-ux-pro-max@mis-skills-claude
/plugin install react-native-skills@mis-skills-claude
/plugin install impeccable@mis-skills-claude
/plugin install marketing-skills@mis-skills-claude
/plugin install task-observer@mis-skills-claude
/plugin install archify@mis-skills-claude
```

| Plugin | Origen | Descripción |
|---|---|---|
| `emil-skills` | [emilkowalski/skills](https://github.com/emilkowalski/skills) | 15 skills de diseño de UI y animación: animate, animate-expo, animation-performance, animation-vocabulary, apple-design, ask-sonner, break-ui, emil-design-eng, find-animation-opportunities, improve-animations, mobile-native, pick-ui-library, prototype, review-animations, write-swift |
| `scroll-world` | [oso95/scroll-world](https://github.com/oso95/scroll-world) | Landing con scroll cinemático: la cámara vuela sin cortes entre escenas 3D generadas con IA. Requiere Higgsfield CLI (y Monid opcional, de pago). |
| `taste-skill` | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) | Skill `design-taste-frontend`: dirección de arte para webs, dashboards y apps, con inspector en navegador real. Requiere Node y Chrome/Chromium. |
| `ui-ux-pro-max` | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | 7 skills: ui-ux-pro-max, design, design-system, brand, banner-design, slides, ui-styling. Requiere Python 3. Generar logos/iconos con IA necesita `GEMINI_API_KEY` (opcional). |
| `react-native-skills` | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-native-skills) | Skill `vercel-react-native-skills`: 37 reglas de rendimiento y buenas prácticas para React Native y Expo. |
| `impeccable` | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) | `/impeccable` con 24 subcomandos y 4 agentes. ⚠️ Descarga su motor desde GitHub al primer uso, ejecuta hooks automáticos en cada sesión/edición y envía telemetría anónima (desactivar con `DO_NOT_TRACK=1`). |
| `marketing-skills` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | 52 skills de marketing (CRO, copywriting, SEO, ads, cold email, pricing, launch…) + CLIs para 66 herramientas (requieren la API key de cada servicio). |
| `task-observer` | [rebelytics/one-skill-to-rule-them-all](https://github.com/rebelytics/one-skill-to-rule-them-all) | Meta-skill que registra correcciones y patrones en `skill-observations/` de tu proyecto y propone mejoras de skills en una revisión semanal. Licencia CC BY 4.0. |
| `archify` | [tt-a1i/archify](https://github.com/tt-a1i/archify) | Diagramas de arquitectura, secuencia, ERD, workflows, timelines y más como HTML interactivo, con exportación a imagen/SVG/WebM. Requiere Node 18+. |

## Plugins externos (se instalan desde el marketplace de su autor)

Estos no están copiados aquí porque dependen de su propio marketplace o se actualizan muy a menudo.

| Plugin | Instalación | Notas |
|---|---|---|
| `claude-mem` | `/plugin marketplace add thedotmack/claude-mem`<br>`/plugin install claude-mem@thedotmack` | Memoria persistente entre sesiones. Requiere `npx claude-mem install`. ⚠️ Hooks en cada prompt y herramienta, servicio en segundo plano, consume tokens para resumir, telemetría PostHog (desactivar con `DO_NOT_TRACK=1`). |
