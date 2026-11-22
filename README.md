# Docs Lista de Tareas

Documentación del proyecto [lista-tareas](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas). Aquí se registra lo que se va construyendo, HU por HU.

- **Tablero:** https://kevin-stiven-lopez-amaya404.github.io/docs-lista-tareas/
- **Código:** https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas
- **Diseño (Figma):** https://www.figma.com/design/Gx9t5vMuidiEKMKpi1lfhV

## Estructura

| Archivo | Qué contiene |
|---|---|
| `index.html` | Tablero publicado en GitHub Pages: flujo de ramas y estado de cada HU |
| `hu/HU-XX-*.md` | Una ficha por historia de usuario: descripción, criterios de aceptación, diseño, estado e implementación |
| `hu/_plantilla.md` | Plantilla para crear una HU nueva |
| `diseno.md` | Enlaces a pantallas y componentes de Figma, y tokens de diseño |
| `decisiones.md` | Decisiones técnicas y de producto, con fecha y motivo |
| `CHANGELOG.md` | Qué se entregó en cada versión (cada merge de `develop` a `main` en lista-tareas) |

## Cómo se mantiene

Cada avance de una HU en lista-tareas se refleja aquí en el mismo momento:

| Paso en lista-tareas | Qué se actualiza aquí |
|---|---|
| Se crea `feature/HU-XX-...` | Ficha de la HU: estado **En desarrollo** y rama. Tablero: tarjeta a "En desarrollo" |
| PR de la HU fusionado en `develop` | Ficha: estado **En pruebas**, enlace al PR y resumen de la implementación. Tablero: "En pruebas" |
| PR `develop` → `main` (entrega) | Ficha: **Entregado**. Tablero: "Entregado". `CHANGELOG.md`: nueva versión |
| Se decide algo relevante | Nueva entrada en `decisiones.md` |

Aquí solo va el resumen y los enlaces, nunca el código.

Este repo sigue el mismo flujo: rama desde `develop` → PR a `develop` → PR `develop` → `main` para publicar. `main` está protegida.
