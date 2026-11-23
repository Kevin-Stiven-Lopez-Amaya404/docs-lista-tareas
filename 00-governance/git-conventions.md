# Convenciones de Git

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
Mismo flujo en **lista-tareas** y en **docs-lista-tareas** ([ADR-006](../05-architecture/decisions/records/ADR-006-ramas-hun-y-dev.md)).

```
dev ──► huN ──(PR huN → dev, al terminar la HU)──► dev ──(PR "Release: vX.Y.Z", solo en entregas)──► main
```

## Ramas

| Rama | Uso | Se borra |
|------|-----|----------|
| `main` | Producción. Solo recibe el PR "Release" desde `dev`. Protegida | — |
| `dev` | Integración. Solo recibe PR. Protegida | — |
| `huN` (`hu4`, `hu11`…) | Todo el trabajo de una HU. **Mismo nombre en los dos repos** | No, se conserva como historial |
| `chore/descripcion` | Trabajo que no es una HU (mantenimiento, estructura, entregas) | Sí, tras el merge |

## Pull Requests

- **Un solo PR `huN → dev` por repo**, cuando la HU está terminada y probada (CI en verde en lista-tareas). Sin PR intermedios por cambio de estado.
- En docs, el PR de la HU se abre después de fusionar el del código.
- Se usa la plantilla `.github/pull_request_template.md`. Las descripciones largas se pasan con `--body-file`.
- Merge con `gh pr merge --merge`, sin `--delete-branch` en las ramas `huN`.

## Commits

Con el número de la HU: `HU-04: editar una tarea`. Los de `chore/` describen el cambio en una línea.

## Entregas

Solo cuando se decide explícitamente una entrega, en los dos repos a la vez:

1. Rama `chore/release-vX.Y.Z`: en la app `npm version X.Y.Z --no-git-tag-version`; en docs, fichas "Entregado en vX.Y.Z", tablero y [CHANGELOG](../CHANGELOG.md).
2. PR a `dev`, luego PR "Release: vX.Y.Z" `dev → main`.
3. Tag anotado `vX.Y.Z` en `main` (los dos repos) y `gh release create` en la app.
4. Back-merge con un PR `main → dev`.
5. Comprobar el despliegue de Vercel en producción ([10-devops/ci-cd.md](../10-devops/ci-cd.md)).

## Finales de línea

`.gitattributes` con `* text=auto eol=lf` ([ADR-007](../05-architecture/decisions/records/ADR-007-finales-de-linea-y-plantilla-pr.md)).
