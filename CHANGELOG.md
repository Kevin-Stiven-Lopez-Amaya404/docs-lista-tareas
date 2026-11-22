# Historial de entregas

Cada entrega es un PR de `dev` a `main` en lista-tareas, con su etiqueta y su Release en GitHub. La más reciente va arriba.

## v1.0.0 — 2026-11-22

Primera entrega a producción ([Release](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/releases/tag/v1.0.0) · [PR #11](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/11)).

| HU | Qué hace | PR |
|---|---|---|
| [HU-01](hu/HU-01-crear-tarea.md) | Crear una tarea: campo y botón Agregar (deshabilitado si está vacío), Enter para agregar | [#3](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/3) |
| [HU-02](hu/HU-02-ver-lista.md) | Ver la lista: resumen "N pendientes · M completadas" y estado vacío | [#4](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/4) |
| [HU-03](hu/HU-03-completar-tarea.md) | Marcar como completada: casilla con check, texto tachado, con teclado | [#5](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/5) |
| [HU-04](hu/HU-04-editar-tarea.md) | Editar una tarea: Guardar/Cancelar, Enter/Escape, una a la vez | [#7](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/7) |
| [HU-05](hu/HU-05-eliminar-tarea.md) | Eliminar una tarea: al instante, con foco accesible | [#8](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/8) |
| [HU-06](hu/HU-06-guardar-tareas.md) | Guardar tareas en el navegador, tolerante a datos dañados | [#9](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/9) |

También: configuración inicial (Vite, Vitest, CI), flujo de ramas `dev`/`huN`.

**Calidad:** 23 pruebas automáticas y build en verde en el CI. Cada HU verificada en el navegador contra sus criterios y el diseño de Figma.

**Pendiente para próximas versiones:** diseño de escritorio (hoy ancho de celular, 390px) y estados hover/focus diseñados en Figma.
