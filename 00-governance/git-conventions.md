# Convenciones de Git

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
Hay **dos modelos de ramas**: el código se trabaja por HU con `dev` y `main`; la documentación se organiza por secciones y vive solo en `main` ([ADR-006](../05-architecture/decisions/records/ADR-006-ramas-hun-y-dev.md), [ADR-010](../05-architecture/decisions/records/ADR-010-docs-no-se-trabajan-por-hu.md)).

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

## docs-lista-tareas (documentación): solo `main`

Igual que [code-sena/design-software-docs](https://github.com/code-sena/design-software-docs): el repo de docs **vive siempre en `main`**, sin `dev` ni ramas por HU. En reposo solo existe `main`.

```
main ──► rama efímera ──(PR → main)──► main   (y se borra la rama)
```

1. Crear una rama efímera desde `main` actualizado.
2. Commit(s) y push.
3. PR hacia `main`, revisar y fusionar con **merge** (se conservan los commits).
4. Borrar la rama.

| Tipo de rama | Cuándo | Ejemplo |
|--------------|--------|---------|
| `docs/…` | Actualizar documentos existentes | `docs/requisitos-hu11` |
| `feat/…` | Documento o sección nueva | `feat/manual-tecnico` |
| `fix/…` | Corregir contenido o enlaces | `fix/enlaces-tablero` |
| `chore/…` | Reorganizar, renombrar o mantenimiento | `chore/estructura-docs` |

**Historial:** las ramas `hu1`…`hu10` que se usaron antes de este modelo están conservadas como etiquetas `archivo/huN` (`git checkout archivo/hu4`), y sus PR siguen en GitHub ([ADR-010](../05-architecture/decisions/records/ADR-010-docs-no-se-trabajan-por-hu.md)).

- No hay ramas `huN` ni fichas por HU: las HU son una sección más de [04-requirements/user-stories.md](../04-requirements/user-stories.md).
- Commits que dicen qué sección cambia: `Requisitos: HU-11 en user-stories y trazabilidad`.
- Qué secciones tocar según el cambio: [docs-touchpoints-matrix.md](./docs-touchpoints-matrix.md).

## Pull Requests (los dos repos)

- Se usa la plantilla `.github/pull_request_template.md`. Las descripciones largas se pasan con `--body-file`.
- Sin commits directos a `main` (ni a `dev` en el código).

## Entregas

Solo cuando se decide explícitamente una entrega del código:

1. **Código:** rama `chore/release-vX.Y.Z` con `npm version X.Y.Z --no-git-tag-version` → PR a `dev` → PR "Release: vX.Y.Z" `dev → main` → tag anotado `vX.Y.Z` y `gh release create` → back-merge con un PR `main → dev`.
2. **Docs:** rama `chore/release-vX.Y.Z` desde `main` con el estado "Entregado en vX.Y.Z" en [user-stories.md](../04-requirements/user-stories.md), tablero, [CHANGELOG](../CHANGELOG.md) y [roadmap](../03-product/roadmap.md) → PR a `main` → tag anotado `vX.Y.Z`.
3. Comprobar el despliegue de Vercel en producción ([10-devops/ci-cd.md](../10-devops/ci-cd.md)).

## Finales de línea

`.gitattributes` con `* text=auto eol=lf` ([ADR-007](../05-architecture/decisions/records/ADR-007-finales-de-linea-y-plantilla-pr.md)).
