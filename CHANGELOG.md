# Historial de entregas

Cada entrega es un PR de `dev` a `main` en lista-tareas, con su etiqueta y su Release en GitHub. La más reciente va arriba.

## v1.2.1 — 2026-11-23 · entrega final

Cierre del proyecto. Publicada en Vercel: https://lista-tareas-sage.vercel.app/ ([Release](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/releases/tag/v1.2.1) · [PR #28](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/28)).

| Cambio | Qué hace | PR |
|---|---|---|
| Favicon | Ícono de pestaña con la casilla marcada del diseño; quita el 404 de `/favicon.ico` | [#26](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/26) |
| Plantilla de PR | Apunta al nuevo flujo de documentación | [#25](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/25) |
| Documentación | Estructura por secciones como code-sena/design-software-docs, HU en un solo documento y repo de docs solo en `main` | [docs#32](https://github.com/Kevin-Stiven-Lopez-Amaya404/docs-lista-tareas/pull/32) |

**Calidad:** 31 pruebas y build en verde, 0 vulnerabilidades en `npm audit`. Revisión en producción antes de la entrega: crear, completar, editar (Escape cancela), filtros, borrar completadas, persistencia al recargar y datos dañados, sin errores en la consola. Después de la entrega: favicon publicado y las 6 cabeceras de seguridad activas.

**Alcance cerrado:** HU-01 a HU-10. **Pendiente conocido:** el diseño de la HU-10 en Figma ([R-01](15-project-control/risks.md)).

## v1.2.0 — 2026-11-22

Publicada en Vercel: https://lista-tareas-sage.vercel.app/ ([Release](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/releases/tag/v1.2.0) · [PR #24](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/24)).

| Cambio | Qué hace | PR |
|---|---|---|
| [HU-09](04-requirements/user-stories.md#hu-09) | Filtros Todas / Pendientes / Completadas, mensaje sin resultados y foco accesible | [#20](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/20) |
| [HU-10](04-requirements/user-stories.md#hu-10) | Botón "Borrar completadas (N)" junto a los filtros | [#21](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/21) |
| Despliegue | Vercel en lugar de GitHub Pages, con `vercel.json` (cabeceras de seguridad y caché) | [#22](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/22) |

**Calidad:** 31 pruebas y build en verde. Verificado en producción: filtros, "Borrar completadas", cabeceras de seguridad activas (CSP, HSTS, `X-Frame-Options`, `nosniff`) y caché inmutable para `/assets/`, sin errores en la consola.

**Pendiente:** el diseño de la HU-10 en Figma, por el límite del conector de Figma en el plan Starter.

## v1.1.1 — 2026-11-22

La app queda publicada: https://kevin-stiven-lopez-amaya404.github.io/lista-tareas/ ([Release](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/releases/tag/v1.1.1) · [PR #19](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/19)).

- **Despliegue automático** ([#17](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/17)): cada entrega a `main` prueba, construye y publica la app en GitHub Pages. Si las pruebas fallan, no se publica.
- **Mantenimiento** ([#16](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/16)): finales de línea LF, plantilla de PR y README actualizado.

Sin cambios de comportamiento respecto a v1.1.0. Verificado en la dirección publicada: carga, agregar, recargar conservando la tarea, íconos y fuente.

## v1.1.0 — 2026-11-22

Diseño completo: versión de escritorio y estados de interacción ([Release](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/releases/tag/v1.1.0) · [PR #15](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/15)).

| HU | Qué hace | PR |
|---|---|---|
| [HU-07](04-requirements/user-stories.md#hu-07) | Versión de escritorio: desde 768px, columna centrada de 640px, más aire y título 36px | [#12](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/12) |
| [HU-08](04-requirements/user-stories.md#hu-08) | Hover según Figma (solo con mouse) y anillo de foco único en todos los controles | [#13](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/13) |

**Calidad:** 23 pruebas automáticas y build en verde. Sin desborde de 320 a 1920px; hover y foco verificados en el navegador; contraste mínimo 6.14:1.

**Compatibilidad:** las tareas guardadas con v1.0.0 se siguen cargando igual.

## v1.0.0 — 2026-11-22

Primera entrega a producción ([Release](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/releases/tag/v1.0.0) · [PR #11](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/11)).

| HU | Qué hace | PR |
|---|---|---|
| [HU-01](04-requirements/user-stories.md#hu-01) | Crear una tarea: campo y botón Agregar (deshabilitado si está vacío), Enter para agregar | [#3](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/3) |
| [HU-02](04-requirements/user-stories.md#hu-02) | Ver la lista: resumen "N pendientes · M completadas" y estado vacío | [#4](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/4) |
| [HU-03](04-requirements/user-stories.md#hu-03) | Marcar como completada: casilla con check, texto tachado, con teclado | [#5](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/5) |
| [HU-04](04-requirements/user-stories.md#hu-04) | Editar una tarea: Guardar/Cancelar, Enter/Escape, una a la vez | [#7](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/7) |
| [HU-05](04-requirements/user-stories.md#hu-05) | Eliminar una tarea: al instante, con foco accesible | [#8](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/8) |
| [HU-06](04-requirements/user-stories.md#hu-06) | Guardar tareas en el navegador, tolerante a datos dañados | [#9](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/9) |

También: configuración inicial (Vite, Vitest, CI), flujo de ramas `dev`/`huN`.

**Calidad:** 23 pruebas automáticas y build en verde en el CI. Cada HU verificada en el navegador contra sus criterios y el diseño de Figma.

**Pendiente para próximas versiones:** diseño de escritorio y estados hover/focus en Figma (resuelto en v1.1.0).
