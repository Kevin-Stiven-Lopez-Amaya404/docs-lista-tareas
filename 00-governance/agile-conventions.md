# Convenciones ágiles

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
## Identificadores

| Prefijo | Significado | Ejemplo |
|---------|-------------|---------|
| `HU-XX` | Historia de usuario | `HU-09` |
| `RF-XX` | Requisito funcional | `RF-07` |
| `NFR-<CAT>-XX` | Requisito no funcional | `NFR-A11Y-01` |
| `RN-XX` | Regla de negocio ([02-domain](../02-domain/entities-and-rules.md)) | `RN-01` |
| `ADR-NNN` | Decisión de arquitectura | `ADR-005` |

## Estados de una HU

| Estado | Cuándo |
|--------|--------|
| Por hacer | Tiene su sección en [user-stories.md](../04-requirements/user-stories.md) y cumple la [Definition of Ready](./definition-of-ready.md) |
| En desarrollo | Existe la rama `huN` en lista-tareas |
| En pruebas | Fusionada en `dev` en lista-tareas |
| Entregado en vX.Y.Z | Llegó a `main` en una entrega |

## Tablero

El tablero es `index.html` en la raíz, publicado en GitHub Pages desde `main`. Cada HU tiene una tarjeta con un resumen corto y "vX.Y.Z · PR #N" (o "dev · PR #N" antes de la entrega). El estado del día a día se ve en la rama `dev`.
