# Diseño

El diseño se hace en Figma y es la fuente de verdad: la interfaz se construye a partir de él.

**Archivo:** https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV

## Pantallas (390 × 844)

| Pantalla | HU | Enlace |
|---|---|---|
| Principal | HU-01, 02, 03, 05 | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-41) |
| Vacía | HU-01, 02 | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-72) |
| Editando | HU-04 | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-127) |

Pendiente de diseñar: versión de escritorio y estados de foco/hover.

## Componentes

| Componente | Variantes | Enlace |
|---|---|---|
| Tarea | `estado`: pendiente, completada, editando | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=1-40) |
| Botón | `tipo`: primario, secundario · `estado`: normal, deshabilitado | [Abrir](https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV?node-id=2-61) |

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
| `color/sobre-primario` | `#FFFFFF` |
| `color/peligro` | `#C2410C` |
| `espacio/4` · `8` · `12` · `16` · `24` | 4 · 8 · 12 · 16 · 24 px |
| `radio/6` · `radio/12` | 6 · 12 px |

**Tipografía:** Inter — Regular 14/16, Semi Bold 16/18, Bold 28.
