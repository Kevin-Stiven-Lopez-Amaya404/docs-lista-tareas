# ADR-001: Stack: Vite + JavaScript + Vitest

**Estado:** ACCEPTED
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** HU-01

---

## Contexto

Hace falta una app web sencilla para anotar tareas en el navegador, con pruebas automáticas y un build reproducible.

## Decisión

Se decide construir la app **sin framework**, con **Vite** para desarrollo y build, y **Vitest** para pruebas. La lógica de tareas vive en funciones puras (`src/tareas.js`) separadas del DOM (`src/main.js`) para poder probarla. El CI (GitHub Actions) corre pruebas y build en cada PR.

## Consecuencias

### Positivas

- Pocas dependencias (solo `vite` y `vitest` de desarrollo) y build rápido.
- La lógica se prueba sin navegador.

### Negativas / Trade-offs

- El DOM se maneja a mano en `main.js`; si la interfaz crece mucho, conviene revisar un framework.

## Alternativas consideradas

| Alternativa | Por qué se descartó |
|-------------|---------------------|
| React / Vue | Más dependencias y conceptos de los que necesita una lista de tareas |
| Jest | Vitest usa la misma configuración que Vite y no necesita transpilar aparte |

## Referencias

- Registro original: [99-archive/old-decisions/decisiones.md](../../../99-archive/old-decisions/decisiones.md)
