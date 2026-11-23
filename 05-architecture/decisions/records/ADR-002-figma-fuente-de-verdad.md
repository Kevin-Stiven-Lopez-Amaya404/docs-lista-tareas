# ADR-002: Diseño en Figma como fuente de verdad

**Estado:** ACCEPTED
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** HU-01

---

## Contexto

La interfaz necesita un diseño consistente (colores, tipografía, espacios) que no se invente en el código.

## Decisión

Se decide que **el diseño se hace en Figma y es la fuente de verdad**. Los tokens de la colección "Tokens" se pasan al código como variables CSS con el mismo nombre (`color/fondo` → `--color-fondo`). Ver [design-system.md](../../../12-ux-ui/design-system.md).

## Consecuencias

### Positivas

- Diseño y código usan los mismos nombres de tokens.

### Negativas / Trade-offs

- El conector de Figma del plan Starter tiene un límite de llamadas: la HU-10 quedó sin diseño en Figma (ver [riesgos](../../../15-project-control/risks.md)).

## Alternativas consideradas

| Alternativa | Por qué se descartó |
|-------------|---------------------|
| Diseñar directamente en CSS | Sin una referencia visual compartida ni revisión previa |

## Referencias

- Registro original: [99-archive/old-decisions/decisiones.md](../../../99-archive/old-decisions/decisiones.md)
