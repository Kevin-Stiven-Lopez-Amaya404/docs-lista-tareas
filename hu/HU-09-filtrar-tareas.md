# HU-09: Filtrar tareas

| | |
|---|---|
| **Estado** | En pruebas (en `dev` desde 2026-11-22) |
| **Rama** | `hu9` |
| **PR** | [lista-tareas#20](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/20) |
| **Diseño** | Componente [Filtros](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=21-132) en [Principal](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) y [Escritorio](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=17-82) · pantalla [Filtro sin resultados](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=21-153) |

## Historia

Como **usuario con muchas tareas**, quiero **ver solo las pendientes o solo las completadas** para **concentrarme en lo que me falta o revisar lo que ya hice**.

## Criterios de aceptación

- [x] Con al menos una tarea, se muestran tres filtros: **Todas**, **Pendientes** y **Completadas**. Al abrir está activo **Todas**.
- [x] Al elegir un filtro, la lista muestra solo esas tareas y el filtro activo se ve marcado (y se anuncia como presionado a los lectores de pantalla).
- [x] El resumen "N pendientes · M completadas" sigue contando todas las tareas.
- [x] Si el filtro no tiene tareas, se muestra "No hay tareas pendientes." o "No hay tareas completadas.".
- [x] Si al marcar o desmarcar una tarea esta deja de verse por el filtro, el foco pasa a la tarea siguiente visible o, si no hay, al filtro activo.
- [x] Una tarea nueva se agrega como pendiente: si el filtro es **Completadas**, se cambia a **Todas** para que se vea.

## Implementación

- **Diseño (Figma):** componente "Opción de filtro" (`activo` sí/no, propiedad Texto) y componente "Filtros" con Todas, Pendientes y Completadas, agregado a Principal y Escritorio. Pantalla nueva "Filtro sin resultados".
- **Lógica:** `src/tareas.js` → `filtrarTareas(tareas, filtro)`. Un filtro desconocido se trata como Todas, para que nunca se oculten tareas por error.
- **Interfaz:** en `index.html`, un grupo `role="group"` con tres botones `aria-pressed` y el párrafo `#sin-resultados`. En `src/main.js`, el estado `filtro` vive solo en memoria y no se guarda; al abrir siempre es Todas. `render()` dibuja solo las visibles y oculta los filtros si no hay tareas. `enfocarCerca()` mueve el foco a la tarea que ocupa el lugar, a la anterior o al filtro activo. Al agregar con Completadas se cambia a Todas.
- **Estilos:** `.filtros` y `.filtro` (activo con `--color-primario`, hover con `--color-fondo` solo con mouse, foco con el anillo común de la HU-08) y `.sin-resultados`.
- **Pruebas:** 4 nuevas (todas, pendientes/completadas, filtro desconocido, resumen): 27 en total. Verificado en el navegador: filtros ocultos sin tareas, Pendientes, marcar dentro del filtro (el foco pasa a la siguiente, luego a la anterior y luego al filtro activo), mensaje sin resultados, agregar con Completadas activo y anillo de foco con Tab.
