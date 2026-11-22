# HU-02: Ver la lista de tareas

| | |
|---|---|
| **Estado** | En pruebas (en `develop` desde 2026-11-22) |
| **Rama** | `feature/HU-02-ver-lista` (fusionada y eliminada) |
| **PR** | [lista-tareas#4](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/4) |
| **Diseño** | [Principal](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) · [Vacía](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-72) |

## Historia

Como **usuario**, quiero **ver todas mis tareas en una lista** para **saber qué tengo pendiente**.

## Criterios de aceptación

- [x] Las tareas se muestran en el orden en que se agregaron.
- [x] Debajo del título se ve el resumen "N pendientes · M completadas".
- [x] Si no hay tareas, se muestra "Aún no tienes tareas" y "Escribe tu primera tarea arriba y pulsa Agregar."

## Implementación

- **Lógica:** `src/tareas.js` → `resumen(tareas)`. Devuelve "Sin tareas todavía" si la lista está vacía; si no, "N pendiente(s) · M completada(s)" con singular y plural.
- **Interfaz:** el resumen va bajo el título (`#resumen`, con `aria-live` para lectores de pantalla). El bloque de estado vacío (`#estado-vacio`) se muestra solo sin tareas y la lista solo cuando hay alguna.
- **Estilos:** `src/estilos.css`: resumen 14px gris, estado vacío centrado (título Semi Bold 18, ayuda 14), igual que la pantalla "Vacía" de Figma.
- **Pruebas:** 3 nuevas en `src/tareas.test.js` (vacío, plural, singular y cero): 7 en total. Verificado en el navegador: estado vacío al abrir, resumen "1 pendiente · 0 completadas" y luego "3 pendientes · 0 completadas", orden conservado.
- **Nota:** el contador de completadas quedará en 0 hasta la HU-03.
