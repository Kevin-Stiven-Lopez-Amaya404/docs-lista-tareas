# Estrategia de pruebas

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
## Automáticas (Vitest)

| Archivo | Qué cubre |
|---------|-----------|
| `src/tareas.test.js` | Toda la lógica pura: agregar, completar, editar, eliminar, borrar completadas, filtrar, resumen, y que nunca se modifica la lista original |
| `src/almacenamiento.test.js` | Cargar y guardar con un almacén falso: JSON dañado, elementos inválidos, almacenamiento bloqueado |

31 pruebas en v1.2.1. Corren en el CI en cada PR ([10-devops/ci-cd.md](../10-devops/ci-cd.md)).

## Verificación manual en navegador

Por cada HU, antes del PR:

- [ ] Criterios de aceptación uno por uno.
- [ ] 390px (celular) y 1440px (escritorio); sin desborde de 320px a 1920px.
- [ ] Solo con teclado: Tab, Enter, Espacio, Escape; el foco siempre visible y nunca perdido.
- [ ] Comparación con el frame de Figma.
- [ ] Recargar la página y comprobar que se conserva lo guardado.
- [ ] Consola sin errores.

## Revisión

Cada PR usa la plantilla `.github/pull_request_template.md` y no se fusiona sin el CI en verde.
