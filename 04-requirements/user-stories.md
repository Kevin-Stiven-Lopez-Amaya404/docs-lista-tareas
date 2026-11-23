# Historias de usuario

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas

Todas las historias de usuario de lista-tareas en un solo documento: historia, criterios de aceptación, diseño, estado y PR del código. El detalle de implementación vive en el PR de cada HU en lista-tareas. Para agregar una HU, copia la [plantilla](./_template-hu.md) al final de este archivo.

| HU | Título | Estado |
|----|--------|--------|
| [HU-01](#hu-01) | Crear una tarea | Entregado en v1.0.0 (2026-11-22) |
| [HU-02](#hu-02) | Ver la lista de tareas | Entregado en v1.0.0 (2026-11-22) |
| [HU-03](#hu-03) | Marcar tarea como completada | Entregado en v1.0.0 (2026-11-22) |
| [HU-04](#hu-04) | Editar una tarea | Entregado en v1.0.0 (2026-11-22) |
| [HU-05](#hu-05) | Eliminar una tarea | Entregado en v1.0.0 (2026-11-22) |
| [HU-06](#hu-06) | Guardar tareas al cerrar el navegador | Entregado en v1.0.0 (2026-11-22) |
| [HU-07](#hu-07) | Versión de escritorio | Entregado en v1.1.0 (2026-11-22) |
| [HU-08](#hu-08) | Estados al pasar el mouse y al enfocar | Entregado en v1.1.0 (2026-11-22) |
| [HU-09](#hu-09) | Filtrar tareas | Entregado en v1.2.0 (2026-11-22) |
| [HU-10](#hu-10) | Borrar las completadas | Entregado en v1.2.0 (2026-11-22) |

## HU-01

**Crear una tarea**

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#3](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/3) |
| **Diseño** | [Principal](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) · [Vacía](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-72) |

Como **usuario**, quiero **escribir una tarea y agregarla a mi lista** para **no olvidar lo que tengo que hacer**.

**Criterios de aceptación**

- [x] Hay un campo de texto con el placeholder "Escribe una nueva tarea…" y un botón **Agregar**.
- [x] El botón **Agregar** está deshabilitado mientras el campo esté vacío o solo tenga espacios.
- [x] Al pulsar **Agregar** o presionar Enter, la tarea aparece en la lista como pendiente.
- [x] Después de agregar, el campo se vacía y conserva el foco para escribir otra.
- [x] Se eliminan los espacios al inicio y al final del texto.

## HU-02

**Ver la lista de tareas**

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#4](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/4) |
| **Diseño** | [Principal](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) · [Vacía](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-72) |

Como **usuario**, quiero **ver todas mis tareas en una lista** para **saber qué tengo pendiente**.

**Criterios de aceptación**

- [x] Las tareas se muestran en el orden en que se agregaron.
- [x] Debajo del título se ve el resumen "N pendientes · M completadas".
- [x] Si no hay tareas, se muestra "Aún no tienes tareas" y "Escribe tu primera tarea arriba y pulsa Agregar."

## HU-03

**Marcar tarea como completada**

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#5](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/5) |
| **Diseño** | [Componente Tarea](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-40) (variantes pendiente / completada) |

Como **usuario**, quiero **marcar una tarea como completada** para **ver mi avance**.

**Criterios de aceptación**

- [x] Cada tarea tiene una casilla; al marcarla, la tarea queda completada (casilla azul y texto tachado en gris).
- [x] Al desmarcarla, la tarea vuelve a pendiente.
- [x] El resumen de pendientes y completadas se actualiza.
- [x] La casilla funciona con teclado (Tab y Espacio).

## HU-04

**Editar una tarea**

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#7](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/7) |
| **Diseño** | [Editando](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-127) · [Componente Tarea](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-40) (variante editando) |

Como **usuario**, quiero **cambiar el texto de una tarea** para **corregirla sin borrarla y crearla de nuevo**.

**Criterios de aceptación**

- [x] Al pulsar el ícono de editar, la tarea pasa a modo edición con su texto actual en un campo.
- [x] **Guardar** (o Enter) aplica el cambio; **Cancelar** (o Escape) deja el texto como estaba.
- [x] No se puede guardar un texto vacío.
- [x] Solo una tarea puede estar en edición a la vez.

## HU-05

**Eliminar una tarea**

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#8](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/8) |
| **Diseño** | [Principal](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) (ícono de eliminar en cada tarea) |

Como **usuario**, quiero **eliminar una tarea** para **mantener mi lista limpia**.

**Criterios de aceptación**

- [x] Al pulsar el ícono de eliminar, la tarea desaparece de la lista de inmediato (sin confirmación).
- [x] El resumen de pendientes y completadas se actualiza.
- [x] Si se elimina la última tarea, se muestra el estado vacío.

## HU-06

**Guardar tareas al cerrar el navegador**

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#9](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/9) |
| **Diseño** | No tiene interfaz |

Como **usuario**, quiero **que mis tareas sigan ahí cuando vuelva a abrir la página** para **no perderlas**.

**Criterios de aceptación**

- [x] Las tareas (texto y estado) se guardan en el navegador (`localStorage`) cada vez que cambian.
- [x] Al abrir la página, se cargan las tareas guardadas.
- [x] Si los datos guardados están dañados o el navegador no permite guardar, la app abre con la lista vacía y sigue funcionando.

## HU-07

**Versión de escritorio**

| | |
|---|---|
| **Estado** | Entregado en v1.1.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#12](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/12) |
| **Diseño** | [Escritorio](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=17-82) (1440 × 900, columna de 640px) |

Como **usuario en computador**, quiero **que la lista aproveche mejor la pantalla** para **leer y usar mis tareas con comodidad**, sin que se vea como un celular angosto.

**Criterios de aceptación**

- [x] Desde 768px de ancho, la lista se muestra en una columna centrada de hasta 640px, con más espacio arriba y un título más grande, según el diseño de escritorio de Figma.
- [x] En celular (menos de 768px) se ve igual que en v1.0.0.
- [x] Nada se desborda horizontalmente entre 320px y 1920px de ancho, incluso con textos de tarea muy largos.

## HU-08

**Estados al pasar el mouse y al enfocar**

| | |
|---|---|
| **Estado** | Entregado en v1.1.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#13](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/13) |
| **Diseño** | [Estados de interacción](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=19-130) · estilo de efecto `Foco/Anillo` · variantes hover/foco del [Botón](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-61) |

Como **usuario**, quiero **ver qué control estoy por usar, con el mouse o con el teclado**, para **saber dónde estoy y qué va a pasar al hacer clic o pulsar una tecla**.

**Criterios de aceptación**

- [x] Al pasar el mouse, los botones Agregar, Guardar y Cancelar, los íconos de editar y eliminar y la casilla cambian de apariencia según Figma. En pantallas táctiles el cambio no se queda "pegado".
- [x] Un botón deshabilitado no cambia al pasar el mouse.
- [x] Todo control enfocado con el teclado muestra el mismo anillo de foco (2px del color de superficie + 2px azul), también en el modo de alto contraste de Windows.
- [x] El texto sobre el color de hover mantiene un contraste de al menos 4.5:1.

## HU-09

**Filtrar tareas**

| | |
|---|---|
| **Estado** | Entregado en v1.2.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#20](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/20) |
| **Diseño** | Componente [Filtros](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=21-132) en [Principal](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) y [Escritorio](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=17-82) · pantalla [Filtro sin resultados](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=21-153) |

Como **usuario con muchas tareas**, quiero **ver solo las pendientes o solo las completadas** para **concentrarme en lo que me falta o revisar lo que ya hice**.

**Criterios de aceptación**

- [x] Con al menos una tarea, se muestran tres filtros: **Todas**, **Pendientes** y **Completadas**. Al abrir está activo **Todas**.
- [x] Al elegir un filtro, la lista muestra solo esas tareas y el filtro activo se ve marcado (y se anuncia como presionado a los lectores de pantalla).
- [x] El resumen "N pendientes · M completadas" sigue contando todas las tareas.
- [x] Si el filtro no tiene tareas, se muestra "No hay tareas pendientes." o "No hay tareas completadas.".
- [x] Si al marcar o desmarcar una tarea esta deja de verse por el filtro, el foco pasa a la tarea siguiente visible o, si no hay, al filtro activo.
- [x] Una tarea nueva se agrega como pendiente: si el filtro es **Completadas**, se cambia a **Todas** para que se vea.

## HU-10

**Borrar las completadas**

| | |
|---|---|
| **Estado** | Entregado en v1.2.0 (2026-11-22) |
| **PR (código)** | [lista-tareas#21](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/21) |
| **Diseño** | **Pendiente en Figma**: se alcanzó el límite del conector de Figma (plan Starter). Falta la variante `tipo=texto-peligro` del Botón y la "Barra de lista" en Principal y Escritorio |

Como **usuario**, quiero **borrar de una vez todas las tareas que ya terminé** para **limpiar la lista sin eliminarlas una por una**.

**Criterios de aceptación**

- [x] Si hay al menos una tarea completada, junto a los filtros aparece el botón **Borrar completadas (N)**, donde N es la cantidad de completadas. Si no hay ninguna, el botón no aparece.
- [x] Al pulsarlo se eliminan todas las completadas de inmediato (igual que eliminar una, sin confirmación) y las pendientes quedan en su orden.
- [x] El resumen y la lista se actualizan. Si no quedan tareas, se muestra el estado vacío.
- [x] El foco no se pierde: pasa al filtro activo o, si no quedan tareas, al campo de nueva tarea.
- [x] En celular el botón pasa debajo de los filtros si no cabe al lado, sin desbordar la pantalla.
