# Riesgos

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
| ID | Riesgo | Impacto | Mitigación | Estado |
|----|--------|---------|------------|--------|
| R-01 | El conector de Figma alcanzó el límite del plan Starter (2026-11-22) | La HU-10 no tiene diseño en Figma (pendiente conocido tras el cierre en v1.2.1) | Construir con tokens y componentes existentes y anotarlo en [user-stories.md](../04-requirements/user-stories.md); probar una llamada barata antes de diseñar | Abierto |
| R-02 | Las tareas solo viven en un navegador | Se pierden si el usuario borra los datos del sitio | Está fuera del alcance; se explica en el [manual](../14-training/user-manual.md) | Aceptado |
| R-03 | Eliminar no pide confirmación | Un clic por error borra una tarea | [ADR-004](../05-architecture/decisions/records/ADR-004-eliminar-sin-confirmacion.md); revisar si resulta molesto | Aceptado |
