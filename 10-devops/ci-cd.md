# CI/CD

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
## Integración continua

`.github/workflows/ci.yml` en lista-tareas. Se ejecuta en cada PR y push a `dev` y `main`:

1. `actions/checkout` y `actions/setup-node` (Node 24, caché de npm).
2. `npm ci`
3. `npm test`
4. `npm run build`

El job se llama **`test`** y es check obligatorio para fusionar en `dev` y `main` ([ADR-009](../05-architecture/decisions/records/ADR-009-ramas-protegidas.md)). Si el CI no arranca en un PR, cerrar y reabrir el PR.

## Entrega continua

Vercel está conectado al repositorio ([ADR-008](../05-architecture/decisions/records/ADR-008-despliegue-vercel.md)): cada PR genera una vista previa y cada merge a `main` publica en producción. El proceso completo de una entrega está en [git-conventions.md](../00-governance/git-conventions.md#entregas).

## Después de cada entrega

- [ ] El commit de `main` tiene el estado "Vercel" en verde.
- [ ] La URL de producción carga y funciona (agregar, recargar, filtros).
- [ ] Las cabeceras de seguridad están activas.
