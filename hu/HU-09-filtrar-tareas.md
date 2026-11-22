# HU-09: Filtrar tareas

| | |
|---|---|
| **Estado** | En desarrollo (desde 2026-11-22) |
| **Rama** | `hu9` |
| **PR** | — |
| **Diseño** | Filtros en las pantallas Principal y Escritorio, y pantalla "Filtro sin resultados" en Figma (se agregan en esta HU) |

## Historia

Como **usuario con muchas tareas**, quiero **ver solo las pendientes o solo las completadas** para **concentrarme en lo que me falta o revisar lo que ya hice**.

## Criterios de aceptación

- [ ] Con al menos una tarea, se muestran tres filtros: **Todas**, **Pendientes** y **Completadas**. Al abrir está activo **Todas**.
- [ ] Al elegir un filtro, la lista muestra solo esas tareas y el filtro activo se ve marcado (y se anuncia como presionado a los lectores de pantalla).
- [ ] El resumen "N pendientes · M completadas" sigue contando todas las tareas.
- [ ] Si el filtro no tiene tareas, se muestra "No hay tareas pendientes." o "No hay tareas completadas.".
- [ ] Si al marcar o desmarcar una tarea esta deja de verse por el filtro, el foco pasa a la tarea siguiente visible o, si no hay, al filtro activo.
- [ ] Una tarea nueva se agrega como pendiente: si el filtro es **Completadas**, se cambia a **Todas** para que se vea.

## Implementación

_Pendiente._
