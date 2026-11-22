# HU-08: Estados al pasar el mouse y al enfocar

| | |
|---|---|
| **Estado** | Entregado en v1.1.0 (2026-11-22) |
| **Rama** | `hu8` |
| **PR** | [lista-tareas#13](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/13) |
| **Diseño** | [Estados de interacción](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=19-130) · estilo de efecto `Foco/Anillo` · variantes hover/foco del [Botón](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-61) |

## Historia

Como **usuario**, quiero **ver qué control estoy por usar, con el mouse o con el teclado**, para **saber dónde estoy y qué va a pasar al hacer clic o pulsar una tecla**.

## Criterios de aceptación

- [x] Al pasar el mouse, los botones Agregar, Guardar y Cancelar, los íconos de editar y eliminar y la casilla cambian de apariencia según Figma. En pantallas táctiles el cambio no se queda "pegado".
- [x] Un botón deshabilitado no cambia al pasar el mouse.
- [x] Todo control enfocado con el teclado muestra el mismo anillo de foco (2px del color de superficie + 2px azul), también en el modo de alto contraste de Windows.
- [x] El texto sobre el color de hover mantiene un contraste de al menos 4.5:1.

## Implementación

- **Diseño (Figma):**
  - token nuevo `color/primario-hover` (#1F45A6);
  - estilo de efecto `Foco/Anillo` (dos sombras con spread: 2px `color/superficie` y 4px `color/primario`);
  - variantes `estado=hover` y `estado=foco` para los botones primario y secundario;
  - tablero "Estados de interacción" con botones, íconos, casilla y campo.
  - En Figma, la sombra con spread solo se dibuja si el elemento recorta su contenido y tiene relleno, por eso las variantes de foco tienen *clip content* y relleno de superficie.
- **Foco (código):** una sola regla `:where(input, button):focus-visible` con `box-shadow: var(--anillo-foco)`. Reemplaza las 5 reglas de foco anteriores. Lleva además `outline: 2px solid transparent` para que el modo de alto contraste de Windows dibuje el contorno. Cancelar combina su borde interior con el anillo.
- **Hover (código):** dentro de `@media (hover: hover)` para que en pantallas táctiles no se quede pegado. Agregar y Guardar usan `--color-primario-hover`, con `:not(:disabled)` para que el deshabilitado no cambie. Cancelar y los botones de ícono usan `--color-fondo`. La casilla sin marcar toma el borde `--color-primario`.
- **Contraste medido:** blanco sobre primario-hover 8.54:1; anillo azul sobre fondo 6.14:1; texto sobre fondo (hover de Cancelar) 14.73:1.
- **Verificación:** en el navegador se revisó el hover de cada control (el deshabilitado no cambia) y un recorrido con Tab: campo, Agregar, casilla, editar, campo de edición y Cancelar, todos con el anillo. Las 23 pruebas siguen en verde (solo estilos).
