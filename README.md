# docs-lista-tareas

Repositorio de documentación del proyecto **[lista-tareas](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas)**, una app web para anotar tareas que se guardan en el navegador.

Este repositorio es la fuente de verdad documental del proyecto. Sigue el mismo flujo de ramas que el código (`huN → dev → main`); ver [convenciones de Git](./00-governance/git-conventions.md).

- **App (producción, Vercel):** https://lista-tareas-sage.vercel.app/
- **Tablero:** https://kevin-stiven-lopez-amaya404.github.io/docs-lista-tareas/ ([`index.html`](./index.html))
- **Código:** https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas
- **Diseño (Figma):** https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV

## Reglas rápidas

- Leer [CONTRIBUTING.md](./CONTRIBUTING.md) antes de agregar o mover documentos.
- Registrar cada archivo nuevo en el `README.md` de su sección.
- Aquí va el resumen y los enlaces, nunca el código.
- No publicar credenciales, tokens ni datos personales ([security-rules.md](./00-governance/security-rules.md)).
- Usar `99-archive/` para preservar documentos reemplazados.

## Estructura

| Sección | Descripción | Estado |
|---------|-------------|--------|
| [00-governance](./00-governance/) | Reglas, convenciones y criterios del repo | 🟢 |
| [01-context](./01-context/) | Contexto, alcance y glosario | 🟢 |
| [02-domain](./02-domain/) | Entidad Tarea y reglas de negocio | 🟢 |
| [03-product](./03-product/) | Visión, roadmap y backlog de producto | 🟢 |
| [04-requirements](./04-requirements/) | Requisitos, historias de usuario y trazabilidad | 🟢 |
| [05-architecture](./05-architecture/) | Vista de arquitectura, despliegue y ADRs | 🟢 |
| [06-data](./06-data/) | Modelo de datos en `localStorage` | 🟢 |
| [07-api](./07-api/) | Contratos de API | ⚫ No aplica |
| [08-uml](./08-uml/) | Diagramas (Mermaid) | 🟢 |
| [09-microservices](./09-microservices/) | Catálogo de servicios | ⚫ No aplica |
| [10-devops](./10-devops/) | Setup local, CI/CD y entornos | 🟢 |
| [11-quality](./11-quality/) | Estrategia de pruebas y revisión | 🟢 |
| [12-ux-ui](./12-ux-ui/) | Design system (Figma y tokens) | 🟢 |
| [13-operations](./13-operations/) | Observabilidad, incidentes y backups | ⚫ No aplica |
| [14-training](./14-training/) | Manual de usuario y onboarding | 🟢 |
| [15-project-control](./15-project-control/) | Riesgos y preguntas abiertas | 🟡 |
| [16-technical-manuals](./16-technical-manuals/) | Manuales técnicos | 🔴 |
| [99-archive](./99-archive/) | Documentos reemplazados | 🟢 |

## Estado de íconos

- 🔴 Pendiente — 🟡 En progreso — 🟢 Estable
- ⚫ No aplica / Deprecado

## Documentos de gobierno

- [Guía de contribución](./CONTRIBUTING.md)
- [Reglas de documentación](./00-governance/documentation-rules.md)
- [Convenciones de Git](./00-governance/git-conventions.md)
- [Qué se documenta en cada HU](./00-governance/docs-touchpoints-matrix.md)
- [Definition of Ready](./00-governance/definition-of-ready.md) · [Definition of Done](./00-governance/definition-of-done.md)
- [CHANGELOG](./CHANGELOG.md)
