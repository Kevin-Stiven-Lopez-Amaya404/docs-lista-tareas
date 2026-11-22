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
| `CHANGELOG.md` | Qué se entregó en cada versión (cada merge de `dev` a `main` en lista-tareas) |

## Cómo se mantiene

Mismo flujo que lista-tareas, con la **misma rama `huN` en los dos repos**:

```
dev ──► huN ──(PR huN → dev, al terminar la HU)──► dev ──(PR "Release", solo en entregas)──► main
```

| Momento | Qué se hace aquí |
|---|---|
| Empieza la HU | Se crea la rama `huN` desde `dev` y en ella la ficha pasa a **En desarrollo** |
| La HU se fusiona en `dev` en lista-tareas | En la misma rama `huN`: ficha **En pruebas** con criterios marcados, enlace al PR y resumen de la implementación, y tarjeta del tablero a "En pruebas". Un solo PR `huN → dev` |
| Entrega a producción (PR `dev → main` en lista-tareas) | PR `dev → main` aquí también: fichas **Entregado**, tablero "Entregado" y nueva versión en `CHANGELOG.md` |
| Se decide algo relevante | Nueva entrada en `decisiones.md`, dentro de la rama de la HU |

Aquí solo va el resumen y los enlaces, nunca el código. `main` está protegida y solo cambia en una entrega. Las ramas `huN` se conservan como historial.
