# ADR-006: Flujo de ramas huN → dev → main

**Estado:** ACCEPTED para el código; la parte de docs está reemplazada por [ADR-010](ADR-010-docs-no-se-trabajan-por-hu.md)
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** Todas

---

## Contexto

Al principio se usaba `main` / `develop` / `feature/HU-XX-…` en el código y dos ramas `docs/…` por HU en este repo.

## Decisión

Se decide:

- `develop` pasa a llamarse **`dev`**.
- **Una sola rama `huN` por HU**, con el mismo nombre en lista-tareas y en docs-lista-tareas, que vuelve a `dev` con **un solo PR** cuando la HU está terminada.
- `main` es producción y solo recibe un PR "Release" desde `dev` en una entrega.
- El trabajo que no es una HU va en `chore/descripcion`.

Detalle en [git-conventions.md](../../../00-governance/git-conventions.md).

## Consecuencias

### Positivas

- Una rama = una HU, en los dos repos.
- Las ramas `huN` se conservan como historial.

### Negativas / Trade-offs

- Hay más ramas en el repositorio.

## Alternativas consideradas

| Alternativa | Por qué se descartó |
|-------------|---------------------|
| Solo `main` con ramas efímeras (como el repo de referencia) | No separa lo integrado (`dev`) de lo entregado (`main`) |

## Referencias

- Registro original: [99-archive/old-decisions/decisiones.md](../../../99-archive/old-decisions/decisiones.md)
