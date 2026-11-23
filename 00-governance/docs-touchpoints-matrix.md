# Qué se documenta según el cambio

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
La documentación se actualiza por **sección**, no por HU. Cada fila es lo que se toca en una rama `docs/tema` ([git-conventions.md](./git-conventions.md#docs-lista-tareas-documentación)).

| Cambio | Secciones que se actualizan |
|--------|-----------------------------|
| Se define una HU nueva | [04-requirements/user-stories.md](../04-requirements/user-stories.md) (sección nueva, estado "Por hacer"), [functional.md](../04-requirements/functional.md) o [non-functional.md](../04-requirements/non-functional.md), [traceability-matrix.md](../04-requirements/traceability-matrix.md), [backlog](../03-product/product-backlog.md) |
| Una HU se fusiona en `dev` del código | Estado y criterios en [user-stories.md](../04-requirements/user-stories.md), PR en la [matriz](../04-requirements/traceability-matrix.md), tarjeta del tablero (`index.html`) |
| Cambia el diseño | [12-ux-ui/design-system.md](../12-ux-ui/design-system.md) |
| Cambia la entidad Tarea o lo guardado | [02-domain](../02-domain/entities-and-rules.md) y [06-data](../06-data/models.md) |
| Cambian los módulos del código | [05-architecture/overview.md](../05-architecture/overview.md) y [08-uml](../08-uml/) |
| Se decide algo relevante | ADR nuevo en [05-architecture/decisions/records](../05-architecture/decisions/records/) |
| Cambia el CI o el despliegue | [10-devops](../10-devops/) y [05-architecture/deployment.md](../05-architecture/deployment.md) |
| Cambian las pruebas | [11-quality/testing-strategy.md](../11-quality/testing-strategy.md) |
| Cambia lo que ve el usuario | [14-training/user-manual.md](../14-training/user-manual.md) |
| Aparece un riesgo o una duda | [15-project-control](../15-project-control/) |
| Entrega a producción | Estados "Entregado en vX.Y.Z", tablero, [CHANGELOG](../CHANGELOG.md), [roadmap](../03-product/roadmap.md). PR `dev → main` aquí también |

Varias filas pueden ir en la misma rama y el mismo PR.
