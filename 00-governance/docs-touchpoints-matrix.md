# Qué se documenta en cada momento

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
| Momento | Dónde | Qué se hace |
|---------|-------|-------------|
| Empieza la HU | rama `huN` | Ficha en `04-requirements/user-stories/` en **En desarrollo** |
| La HU se fusiona en `dev` (código) | misma rama `huN` | Ficha en **En pruebas** con criterios marcados, PR y sección "Implementación"; [user-stories.md](../04-requirements/user-stories.md); [traceability-matrix.md](../04-requirements/traceability-matrix.md); tarjeta del tablero. **Un solo PR `huN → dev`** |
| Cambia el diseño | misma rama | [12-ux-ui/design-system.md](../12-ux-ui/design-system.md) |
| Cambia la entidad Tarea o lo guardado | misma rama | [02-domain](../02-domain/entities-and-rules.md) y [06-data](../06-data/models.md) |
| Se decide algo relevante | misma rama | Nuevo ADR en [05-architecture/decisions/records](../05-architecture/decisions/records/) |
| Cambia el CI o el despliegue | rama `chore/` | [10-devops](../10-devops/) |
| Aparece un riesgo o una duda | cualquier rama | [15-project-control](../15-project-control/) |
| Entrega a producción | `chore/release-vX.Y.Z` | Fichas **Entregado en vX.Y.Z**, tablero, [CHANGELOG](../CHANGELOG.md), [roadmap](../03-product/roadmap.md). PR `dev → main` aquí también |
