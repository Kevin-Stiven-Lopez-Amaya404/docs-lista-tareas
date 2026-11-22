# HU-10: Borrar las completadas

| | |
|---|---|
| **Estado** | Entregado en v1.2.0 (2026-11-22) |
| **Rama** | `hu10` |
| **PR** | [lista-tareas#21](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/21) |
| **Diseño** | **Pendiente en Figma**: se alcanzó el límite del conector de Figma (plan Starter). Falta la variante `tipo=texto-peligro` del Botón y la "Barra de lista" en Principal y Escritorio |

## Historia

Como **usuario**, quiero **borrar de una vez todas las tareas que ya terminé** para **limpiar la lista sin eliminarlas una por una**.

## Criterios de aceptación

- [x] Si hay al menos una tarea completada, junto a los filtros aparece el botón **Borrar completadas (N)**, donde N es la cantidad de completadas. Si no hay ninguna, el botón no aparece.
- [x] Al pulsarlo se eliminan todas las completadas de inmediato (igual que eliminar una, sin confirmación) y las pendientes quedan en su orden.
- [x] El resumen y la lista se actualizan. Si no quedan tareas, se muestra el estado vacío.
- [x] El foco no se pierde: pasa al filtro activo o, si no quedan tareas, al campo de nueva tarea.
- [x] En celular el botón pasa debajo de los filtros si no cabe al lado, sin desbordar la pantalla.

## Implementación

- **Lógica:** `src/tareas.js` → `borrarCompletadas(tareas)`.
- **Interfaz:** `.barra-lista` agrupa los filtros y el botón `#borrar-completadas`. Usa flex con *wrap* y `space-between`: en 390px el botón baja debajo de los filtros y en escritorio va en la misma fila. El texto muestra la cantidad, y el botón se oculta si no hay completadas. Al borrar, el foco va al filtro activo o al campo de nueva tarea.
- **Estilos:** `.boton-texto-peligro`, con texto de 14px en `--color-peligro` (contraste 4.79:1 sobre el fondo). El hover usa `--color-superficie` porque el botón va sobre el fondo de la página. El foco usa el anillo común.
- **Diseño:** se construyó solo con tokens y componentes existentes, porque Figma no estaba disponible. Hay que pasarlo a Figma cuando se pueda.
- **Pruebas:** 4 nuevas (quita completadas en orden, sin completadas, todas completadas, no modifica la original): 31 en total. Verificado en el navegador: contador, borrar con pendientes (orden, guardado y foco), borrar todas (estado vacío y foco al campo) y distribución a 390px y 1440px sin desborde.
