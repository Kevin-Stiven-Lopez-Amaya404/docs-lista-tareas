# Diseño

El diseño se hace en Figma y es la fuente de verdad: la interfaz se construye a partir de él.

**Archivo:** https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV

## Pantallas

| Pantalla | Tamaño | HU | Enlace |
|---|---|---|---|
| Principal | 390 × 844 | HU-01, 02, 03, 05 | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) |
| Vacía | 390 × 844 | HU-01, 02 | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-72) |
| Editando | 390 × 844 | HU-04 | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-127) |
| Escritorio | 1440 × 900 | HU-07 | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=17-82) |
| Estados de interacción | tablero | HU-08 | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=19-130) |

**Escritorio (desde 768px):** columna centrada de 640px, `espacio/64` arriba y abajo, título Bold 36 y resumen Regular 16. El resto igual que en celular.

**Estados (HU-08):** hover solo en dispositivos con mouse. Primario → `color/primario-hover`; secundario e íconos → `color/fondo`; casilla sin marcar → borde `color/primario`. Foco con teclado: estilo de efecto `Foco/Anillo` en todos los controles (en CSS, `--anillo-foco`).

## Componentes

| Componente | Variantes | Enlace |
|---|---|---|
| Tarea | `estado`: pendiente, completada, editando | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-40) |
| Botón | `tipo`: primario, secundario · `estado`: normal, hover, foco, deshabilitado (solo primario) | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-61) |

## Tokens (colección "Tokens" en Figma)

En el código se usan como variables CSS con el mismo nombre (`color/fondo` → `--color-fondo`).

| Token | Valor |
|---|---|
| `color/fondo` | `#F5F6F8` |
| `color/superficie` | `#FFFFFF` |
| `color/texto` | `#1B2230` |
| `color/texto-secundario` | `#5D6778` |
| `color/borde` | `#DDE1E8` |
| `color/primario` | `#2754C5` |
| `color/primario-hover` | `#1F45A6` |
| `color/sobre-primario` | `#FFFFFF` |
| `color/peligro` | `#C2410C` |
| `espacio/4` · `8` · `12` · `16` · `24` · `64` | 4 · 8 · 12 · 16 · 24 · 64 px |
| `radio/6` · `radio/12` | 6 · 12 px |

**Tipografía:** Inter — Regular 14/16, Semi Bold 16/18, Bold 28 (Bold 36 en escritorio).

**Efectos:** `Foco/Anillo` — 2px `color/superficie` + 2px `color/primario` alrededor del control (CSS: `0 0 0 2px var(--color-superficie), 0 0 0 4px var(--color-primario)`).
