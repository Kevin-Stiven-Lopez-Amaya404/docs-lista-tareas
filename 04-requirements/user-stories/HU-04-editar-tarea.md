# HU-04: Editar una tarea

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **Rama** | `hu4` |
| **PR** | [lista-tareas#7](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/7) |
| **Diseño** | [Editando](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-127) · [Componente Tarea](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-40) (variante editando) |

## Historia

Como **usuario**, quiero **cambiar el texto de una tarea** para **corregirla sin borrarla y crearla de nuevo**.

## Criterios de aceptación

- [x] Al pulsar el ícono de editar, la tarea pasa a modo edición con su texto actual en un campo.
- [x] **Guardar** (o Enter) aplica el cambio; **Cancelar** (o Escape) deja el texto como estaba.
- [x] No se puede guardar un texto vacío.
- [x] Solo una tarea puede estar en edición a la vez.

## Implementación

- **Lógica:** `src/tareas.js` → `editarTarea(tareas, id, texto)`. Recorta espacios, ignora texto vacío y conserva el estado completada.
- **Interfaz:** `src/main.js` guarda `editandoId` (una sola tarea en edición). Cada tarea tiene un botón de editar con el ícono de Figma (`src/assets/icon-editar.svg`) y `aria-label` "Editar tarea: …". En edición se muestra un formulario con el texto seleccionado, **Cancelar** y **Guardar**. Enter guarda, Escape cancela, Guardar se deshabilita con el campo vacío y al terminar el foco vuelve al botón de editar. Si se abre otra tarea, la edición anterior se descarta.
- **Estilos:** variante `.tarea.editando` (borde de 2px en `--color-primario`, campo sobre `--color-fondo` con radio 6), nuevo `.boton-secundario` (borde interior, misma altura que el primario) y `.boton-icono`.
- **Pruebas:** 4 nuevas en `src/tareas.test.js` (editar con recorte, conservar completada, ignorar vacío, no modificar la original): 15 en total. Verificado en el navegador: Enter guarda, Escape y Cancelar descartan, el vacío no se guarda, una sola edición a la vez, foco con teclado y comparación visual con la variante de Figma.
- **Sin diseño todavía:** estados hover y focus de los botones (se usa el contorno de foco estándar).
