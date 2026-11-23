# Convenciones de Git

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
Los dos repos comparten `main` (producción) y `dev` (integración), pero **solo el código se trabaja por HU**. La documentación se organiza por secciones y se actualiza con ramas cortas por tema ([ADR-006](../05-architecture/decisions/records/ADR-006-ramas-hun-y-dev.md), [ADR-010](../05-architecture/decisions/records/ADR-010-docs-no-se-trabajan-por-hu.md)).

## lista-tareas (código)

```
dev ──► huN ──(PR huN → dev, al terminar la HU)──► dev ──(PR "Release: vX.Y.Z", solo en entregas)──► main
```

| Rama | Uso | Se borra |
|------|-----|----------|
| `main` | Producción. Solo recibe el PR "Release" desde `dev`. Protegida | — |
| `dev` | Integración. Solo recibe PR. Protegida | — |
| `huN` (`hu4`, `hu11`…) | Todo el trabajo de una HU | No, se conserva como historial |
| `chore/descripcion` | Trabajo que no es una HU | Sí, tras el merge |

- **Un solo PR `huN → dev`** cuando la HU está terminada y probada (CI en verde).
- Commits con el número de la HU: `HU-04: editar una tarea`.
- Merge con `gh pr merge --merge`, sin `--delete-branch` en las ramas `huN`.

## docs-lista-tareas (documentación)

```
dev ──► docs/tema ──(PR → dev)──► dev ──(PR "Release: vX.Y.Z", solo en entregas)──► main
```

| Rama | Uso | Se borra |
|------|-----|----------|
| `main` | Lo publicado (GitHub Pages del tablero). Solo recibe el PR "Release" desde `dev`. Protegida | — |
| `dev` | Documentación al día. Solo recibe PR. Protegida | — |
| `docs/tema` (`docs/requisitos-hu11`, `docs/arquitectura`…) | Un cambio de documentación, de una o varias secciones | Sí, tras el merge |
| `chore/descripcion` | Mantenimiento del repo y entregas | Sí, tras el merge |

- No hay ramas `huN` ni fichas por HU: las HU son una sección más de [04-requirements/user-stories.md](../04-requirements/user-stories.md).
- Commits que dicen qué sección cambia: `Requisitos: HU-11 en user-stories y trazabilidad`.
- Qué secciones tocar según el cambio: [docs-touchpoints-matrix.md](./docs-touchpoints-matrix.md).

## Pull Requests (los dos repos)

- Se usa la plantilla `.github/pull_request_template.md`. Las descripciones largas se pasan con `--body-file`.
- Sin commits directos a `dev` ni a `main`.

## Entregas

Solo cuando se decide explícitamente una entrega, en los dos repos a la vez:

1. Rama `chore/release-vX.Y.Z`: en la app `npm version X.Y.Z --no-git-tag-version`; en docs, estado "Entregado en vX.Y.Z" en [user-stories.md](../04-requirements/user-stories.md), tablero, [CHANGELOG](../CHANGELOG.md) y [roadmap](../03-product/roadmap.md).
2. PR a `dev`, luego PR "Release: vX.Y.Z" `dev → main`.
3. Tag anotado `vX.Y.Z` en `main` (los dos repos) y `gh release create` en la app.
4. Back-merge con un PR `main → dev`.
5. Comprobar el despliegue de Vercel en producción ([10-devops/ci-cd.md](../10-devops/ci-cd.md)).

## Finales de línea

`.gitattributes` con `* text=auto eol=lf` ([ADR-007](../05-architecture/decisions/records/ADR-007-finales-de-linea-y-plantilla-pr.md)).
