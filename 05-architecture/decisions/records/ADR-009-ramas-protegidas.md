# ADR-009: Ramas protegidas y una sola dirección pública

**Estado:** ACCEPTED
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** —

---

## Contexto

Después de la v1.2.0 había que evitar cambios directos en `main` y `dev`.

## Decisión

Se decide proteger `main` y `dev` en los dos repos: solo aceptan PR, sin force push ni borrado, también para administradores. En lista-tareas además se exige el check "test" en verde. Tras una entrega, `dev` se sincroniza con un PR `main → dev`. GitHub Pages de la app se apaga: la única dirección es la de Vercel (el tablero de este repo sigue en GitHub Pages).

## Consecuencias

### Positivas

- Nada llega a producción sin PR y CI.

### Negativas / Trade-offs

- Sincronizar `dev` tras una entrega necesita un PR más.

## Referencias

- Registro original: [99-archive/old-decisions/decisiones.md](../../../99-archive/old-decisions/decisiones.md)
