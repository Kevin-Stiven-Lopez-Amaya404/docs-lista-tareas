# HU-07: Versión de escritorio

| | |
|---|---|
| **Estado** | En pruebas (en `dev` desde 2026-11-22) |
| **Rama** | `hu7` |
| **PR** | [lista-tareas#12](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/12) |
| **Diseño** | [Escritorio](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=17-82) (1440 × 900, columna de 640px) |

## Historia

Como **usuario en computador**, quiero **que la lista aproveche mejor la pantalla** para **leer y usar mis tareas con comodidad**, sin que se vea como un celular angosto.

## Criterios de aceptación

- [x] Desde 768px de ancho, la lista se muestra en una columna centrada de hasta 640px, con más espacio arriba y un título más grande, según el diseño de escritorio de Figma.
- [x] En celular (menos de 768px) se ve igual que en v1.0.0.
- [x] Nada se desborda horizontalmente entre 320px y 1920px de ancho, incluso con textos de tarea muy largos.

## Implementación

- **Diseño:** nueva pantalla "Escritorio" en Figma (1440 × 900) hecha con los mismos componentes. Columna de 640px, `espacio/64` arriba y abajo (token nuevo), título Bold 36 y resumen Regular 16.
- **Estilos:** `src/estilos.css` tiene una regla `@media (min-width: 768px)` al final del archivo para que tenga prioridad sobre las de celular. Ancho máximo `640px + 2 × espacio-24`, `padding-block: --espacio-64`, título 36px y resumen 16px. Nuevo token `--espacio-64`.
- **Error encontrado y corregido:** la primera versión dejaba la regla antes de las de celular y el título no cambiaba. Se detectó al medir en el navegador.
- **Verificación:** se midió a 320, 390, 767, 768, 1440 y 1920px con una tarea de texto muy largo sin espacios. No hubo desborde horizontal y el cambio ocurre en 768px. También se hizo una comparación visual con Figma a 1440px. Las 23 pruebas siguen en verde (es un cambio solo de estilos, sin lógica nueva).
