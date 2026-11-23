# Definition of Done

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
## HU de código

Una HU está **terminada** (En pruebas) cuando:

- [ ] Cumple todos sus criterios de aceptación.
- [ ] La lógica nueva tiene pruebas en Vitest y `npm test` y `npm run build` pasan en el CI.
- [ ] Se verificó en el navegador a 390px y 1440px, con mouse y con teclado.
- [ ] Coincide con el diseño de Figma (o el pendiente está anotado en la ficha y en [riesgos](../15-project-control/risks.md)).
- [ ] El PR `huN → dev` está fusionado en lista-tareas.
- [ ] La documentación de la [matriz de touchpoints](./docs-touchpoints-matrix.md) está en el PR `huN → dev` de este repo.

Está **Entregada** cuando llegó a `main` en una entrega y se comprobó en producción.

## Documento

Un documento está terminado cuando:

- [ ] Está enlazado desde el `README.md` de su sección.
- [ ] Su estado es 🟢 (o ⚫ si no aplica).
- [ ] Los enlaces relativos funcionan.
- [ ] No contiene información sensible ([security-rules.md](./security-rules.md)).
