# Requisitos no funcionales

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
| ID | Categoría | Requisito | HU / origen |
|----|-----------|-----------|-------------|
| NFR-UX-01 | Adaptable | Se usa cómodo de 320px a 1920px, sin desborde horizontal; desde 768px, columna de 640px | HU-07 |
| NFR-A11Y-01 | Accesibilidad | Todo se usa con teclado; foco visible igual en todos los controles, también en alto contraste | HU-08 |
| NFR-A11Y-02 | Accesibilidad | Contraste de texto de al menos 4.5:1 | HU-08, HU-10 |
| NFR-A11Y-03 | Accesibilidad | El foco nunca se pierde al eliminar, filtrar o borrar | HU-05, HU-09, HU-10 |
| NFR-REL-01 | Fiabilidad | Datos guardados dañados o almacenamiento bloqueado no rompen la app | HU-06 |
| NFR-SEC-01 | Seguridad | Cabeceras CSP, HSTS, `X-Frame-Options`, `nosniff`, `Referrer-Policy` y `Permissions-Policy` en producción | [ADR-008](../05-architecture/decisions/records/ADR-008-despliegue-vercel.md) |
| NFR-QA-01 | Calidad | La lógica tiene pruebas automáticas y el CI bloquea el merge si fallan | [ADR-001](../05-architecture/decisions/records/ADR-001-stack-vite-javascript-vitest.md) |
