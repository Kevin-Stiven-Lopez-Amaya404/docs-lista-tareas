# HU-10: Borrar las completadas

| | |
|---|---|
| **Estado** | En desarrollo (desde 2026-11-22) |
| **Rama** | `hu10` |
| **PR** | — |
| **Diseño** | Botón "Borrar completadas" junto a los filtros en Figma (se agrega en esta HU) |

## Historia

Como **usuario**, quiero **borrar de una vez todas las tareas que ya terminé** para **limpiar la lista sin eliminarlas una por una**.

## Criterios de aceptación

- [ ] Si hay al menos una tarea completada, junto a los filtros aparece el botón **Borrar completadas (N)**, donde N es la cantidad de completadas. Si no hay ninguna, el botón no aparece.
- [ ] Al pulsarlo se eliminan todas las completadas de inmediato (igual que eliminar una, sin confirmación) y las pendientes quedan en su orden.
- [ ] El resumen y la lista se actualizan. Si no quedan tareas, se muestra el estado vacío.
- [ ] El foco no se pierde: pasa al filtro activo o, si no quedan tareas, al campo de nueva tarea.
- [ ] En celular el botón pasa debajo de los filtros si no cabe al lado, sin desbordar la pantalla.

## Implementación

_Pendiente._
