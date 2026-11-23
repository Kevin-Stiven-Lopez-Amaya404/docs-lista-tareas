# HU-05: Eliminar una tarea

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **Rama** | `hu5` |
| **PR** | [lista-tareas#8](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/8) |
| **Diseño** | [Principal](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) (ícono de eliminar en cada tarea) |

## Historia

Como **usuario**, quiero **eliminar una tarea** para **mantener mi lista limpia**.

## Criterios de aceptación

- [x] Al pulsar el ícono de eliminar, la tarea desaparece de la lista de inmediato (sin confirmación).
- [x] El resumen de pendientes y completadas se actualiza.
- [x] Si se elimina la última tarea, se muestra el estado vacío.

## Implementación

- **Lógica:** `src/tareas.js` → `eliminarTarea(tareas, id)`. Devuelve una lista nueva sin esa tarea y conserva el orden.
- **Interfaz:** botón de eliminar en cada tarea con el ícono de Figma (`src/assets/icon-eliminar.svg`) y `aria-label` "Eliminar tarea: …". Para que el foco no se pierda con teclado, pasa al botón de eliminar de la tarea que ocupa su lugar, a la anterior o, si la lista queda vacía, al campo de nueva tarea. Se creó `crearBotonIcono()` para compartir el botón con editar.
- **Pruebas:** 3 nuevas en `src/tareas.test.js` (quita solo la indicada, resumen y estado vacío, no modifica la original): 18 en total. Verificado en el navegador con mouse y teclado hasta dejar la lista vacía, y comparación visual con la pantalla Principal de Figma.
