# ADR-008: Despliegue con Vercel

**Estado:** ACCEPTED (reemplaza GitHub Pages)
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** —

---

## Contexto

La v1.1.1 se publicó en GitHub Pages, pero el equipo despliega sus proyectos con Vercel.

## Decisión

Se decide desplegar con **Vercel**, conectado al repositorio de GitHub: cada merge a `main` publica en producción (https://lista-tareas-sage.vercel.app/) y cada PR genera una vista previa. `vercel.json` (lista-tareas#22) define build de Vite hacia `dist`, cabeceras de seguridad (CSP que solo permite Google Fonts, `nosniff`, `X-Frame-Options: DENY`, HSTS, `Referrer-Policy`, `Permissions-Policy`) y caché inmutable para `/assets/`. Se quitó el workflow de GitHub Pages.

## Consecuencias

### Positivas

- Vistas previas por PR.
- Cabeceras de seguridad y caché en un solo archivo.

### Negativas / Trade-offs

- La dirección de GitHub Pages de la v1.1.1 queda obsoleta.

## Alternativas consideradas

| Alternativa | Por qué se descartó |
|-------------|---------------------|
| GitHub Pages | No permite cabeceras HTTP propias ni vistas previas por PR |

## Referencias

- [05-architecture/deployment.md](../../deployment.md)
- Registro original: [99-archive/old-decisions/decisiones.md](../../../99-archive/old-decisions/decisiones.md)
