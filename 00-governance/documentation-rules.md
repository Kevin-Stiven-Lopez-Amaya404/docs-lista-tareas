# Reglas de documentación

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
## Nombres

- Carpetas numeradas `NN-tema/`, en minúsculas y en inglés, igual que la estructura de referencia.
- Archivos en `kebab-case.md`. Las plantillas empiezan con `_template-`.
- Historias: una sección `## HU-XX` en `04-requirements/user-stories.md` (no hay un archivo por HU). Decisiones: `05-architecture/decisions/records/ADR-NNN-titulo-corto.md`.
- El contenido se escribe en español.

## Cabecera mínima

Cada documento (salvo ADR y plantillas, que tienen la suya) empieza con:

```
# Título

> Estado: 🟢 Estable | Última actualización: AAAA-MM-DD
> Autor: <usuario> | Equipo: lista-tareas
```

## Estados

🔴 Pendiente · 🟡 En progreso · 🟢 Estable · ⚫ No aplica / Deprecado.

## Índices

- Cada carpeta tiene un `README.md` con la tabla de sus archivos.
- Un archivo nuevo no está terminado hasta que aparece en el índice de su sección.
- El `README.md` raíz lista las secciones y su estado.

## Diagramas

En Mermaid, dentro del Markdown, para que GitHub los dibuje y se puedan editar como texto (ver [08-uml](../08-uml/)).

## Enlaces

Relativos entre documentos de este repo. Al código, a Figma y a Vercel, absolutos.
