# HU-03: Marcar tarea como completada

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **Rama** | `feature/HU-03-completar-tarea` (fusionada y eliminada) |
| **PR** | [lista-tareas#5](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/5) |
| **Diseño** | [Componente Tarea](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-40) (variantes pendiente / completada) |

## Historia

Como **usuario**, quiero **marcar una tarea como completada** para **ver mi avance**.

## Criterios de aceptación

- [x] Cada tarea tiene una casilla; al marcarla, la tarea queda completada (casilla azul y texto tachado en gris).
- [x] Al desmarcarla, la tarea vuelve a pendiente.
- [x] El resumen de pendientes y completadas se actualiza.
- [x] La casilla funciona con teclado (Tab y Espacio).

## Implementación

- **Lógica:** `src/tareas.js` → `alternarCompletada(tareas, id)`. Devuelve una lista nueva con esa tarea alternada entre pendiente y completada.
- **Interfaz:** cada tarea es un `label` con una casilla nativa (`input type="checkbox"`) y el texto, así que también se marca al hacer clic en el texto. Un solo escuchador `change` en la lista; después de redibujar, el foco vuelve a la misma casilla para que el teclado siga funcionando.
- **Estilos:** casilla de 22px con borde gris de 2px y radio 6. Marcada: fondo `--color-primario` con el ícono de check exportado de Figma (`src/assets/icon-check.svg`). Completada: texto tachado en `--color-texto-secundario`.
- **Pruebas:** 4 nuevas en `src/tareas.test.js` (marca solo la indicada, desmarca, no modifica la original, actualiza el resumen): 11 en total. Verificado en el navegador con mouse y teclado (Shift+Tab y Espacio).
