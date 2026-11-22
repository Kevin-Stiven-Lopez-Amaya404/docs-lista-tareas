# HU-01: Crear una tarea

| | |
|---|---|
| **Estado** | En pruebas (en `develop` desde 2026-11-22) |
| **Rama** | `feature/HU-01-crear-tarea` (fusionada y eliminada) |
| **PR** | [lista-tareas#3](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/3) |
| **Diseño** | [Principal](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) · [Vacía](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-72) |

## Historia

Como **usuario**, quiero **escribir una tarea y agregarla a mi lista** para **no olvidar lo que tengo que hacer**.

## Criterios de aceptación

- [x] Hay un campo de texto con el placeholder "Escribe una nueva tarea…" y un botón **Agregar**.
- [x] El botón **Agregar** está deshabilitado mientras el campo esté vacío o solo tenga espacios.
- [x] Al pulsar **Agregar** o presionar Enter, la tarea aparece en la lista como pendiente.
- [x] Después de agregar, el campo se vacía y conserva el foco para escribir otra.
- [x] Se eliminan los espacios al inicio y al final del texto.

## Implementación

- **Lógica:** `src/tareas.js` → `agregarTarea(tareas, texto)`. Función pura: recorta espacios, ignora texto vacío y devuelve una lista nueva con `{ id, texto, completada: false }`.
- **Interfaz:** `index.html` + `src/main.js`. Formulario con campo y botón; el botón se habilita según el texto; al enviar se agrega, se vacía el campo y se mantiene el foco. Cada tarea se muestra como tarjeta (solo texto por ahora).
- **Estilos:** `src/estilos.css` con los tokens de Figma como variables CSS (`--color-*`, `--espacio-*`, `--radio-*`) y fuente Inter. Ancho máximo 390px (diseño móvil) hasta que exista el diseño de escritorio.
- **Pruebas:** `src/tareas.test.js`, 4 pruebas (agregar, recortar espacios, ignorar vacío, no modificar la lista original). Verificado también en el navegador.
- **Pendiente para otras HU:** casilla y botones de editar/eliminar en cada tarjeta (HU-03/04/05), resumen y estado vacío (HU-02). Las tareas aún no se guardan al recargar (HU-06).
