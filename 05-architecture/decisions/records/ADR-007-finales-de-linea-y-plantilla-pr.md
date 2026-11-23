# ADR-007: Finales de línea LF y plantilla de PR

**Estado:** ACCEPTED
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** —

---

## Contexto

En Windows, `core.autocrlf=true` mezclaba CRLF y LF en los archivos editados.

## Decisión

Se decide añadir `.gitattributes` con `* text=auto eol=lf` en los dos repos y una plantilla `.github/pull_request_template.md` con la lista de verificación de cada PR.

## Consecuencias

### Positivas

- Diffs limpios en cualquier sistema operativo.
- Cada PR revisa lo mismo.

## Referencias

- Registro original: [99-archive/old-decisions/decisiones.md](../../../99-archive/old-decisions/decisiones.md)
