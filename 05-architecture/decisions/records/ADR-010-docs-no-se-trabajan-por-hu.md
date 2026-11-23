# ADR-010: La documentación no se trabaja por HU

**Estado:** ACCEPTED (reemplaza la parte de docs de [ADR-006](ADR-006-ramas-hun-y-dev.md))
**Fecha:** 2026-11-23
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** —

---

## Contexto

Con [ADR-006](ADR-006-ramas-hun-y-dev.md), docs-lista-tareas usaba la misma rama `huN` que el código y una ficha por HU (`hu/HU-XX-*.md`). Al pasar a la estructura por secciones (como code-sena/design-software-docs), las fichas repetían lo que ya está en requisitos, arquitectura, datos y diseño, y el repo quedaba desordenado.

## Decisión

Se decide que **la documentación se organiza por secciones y no por HU**:

- Las HU son una sección más: todas en [04-requirements/user-stories.md](../../../04-requirements/user-stories.md), con historia, criterios, estado, diseño y PR. Se eliminan las fichas individuales.
- El repo de docs no usa ramas `huN`: cada cambio va en una rama corta `docs/tema` → PR a `dev`, y la rama se borra tras el merge.
- `main` sigue recibiendo solo el PR "Release" en una entrega, a la vez que el código.
- El código (lista-tareas) sigue con `huN` ([ADR-006](ADR-006-ramas-hun-y-dev.md)).

## Consecuencias

### Positivas

- Cada dato está en un solo sitio (requisitos, arquitectura, datos…).
- Se puede documentar varias HU o temas en un PR, o una sección sin HU.

### Negativas / Trade-offs

- El detalle de implementación de cada HU ya no está en docs: queda en el PR del código y en el historial de git de este repo.

## Referencias

- [00-governance/git-conventions.md](../../../00-governance/git-conventions.md)
- [00-governance/docs-touchpoints-matrix.md](../../../00-governance/docs-touchpoints-matrix.md)
