# Decisiones

Registro de decisiones técnicas y de producto. La más reciente va arriba.

## 2026-11-22 — Ramas `huN` y `dev` (reemplaza el flujo anterior)

- `develop` se renombra a `dev`.
- Una sola rama por HU, `huN` (`hu4`, `hu5`…), con el **mismo nombre en lista-tareas y en este repo**. Lleva todo el trabajo de la HU y se une a `dev` con **un solo PR** cuando está terminada y probada (CI en verde). Antes se usaban `feature/HU-XX-…` en el código y dos ramas `docs/…` por HU aquí.
- Las ramas `huN` se conservan como historial. HU-01 a HU-03 tienen `hu1`, `hu2` y `hu3` creadas después sobre su merge en `dev`.
- `main` es producción: solo recibe un PR "Release" desde `dev` cuando se decide una entrega, en los dos repos a la vez.
- Tareas que no son una HU: `chore/descripcion`.

## 2026-11-22 — Eliminar sin confirmación

Al pulsar eliminar, la tarea se borra de inmediato, sin diálogo ni "deshacer". Es una lista personal y simple. Se puede revisar si resulta molesto.

## 2026-11-22 — Agregar deshabilitado con el campo vacío

El botón **Agregar** se deshabilita mientras no haya texto, para evitar tareas en blanco sin mostrar mensajes de error.

## 2026-11-22 — Diseño en Figma

El diseño se hace en Figma y es la fuente de verdad. Los tokens de Figma se pasan al código como variables CSS. Ver [diseno.md](diseno.md).

## 2026-11-22 — Stack: Vite + JavaScript + Vitest

App web sin framework, con Vite para desarrollo y build, y Vitest para pruebas. Es lo más simple para una lista de tareas en el navegador. El CI (GitHub Actions) ejecuta pruebas y build en cada PR.

## 2026-11-22 — Flujo de ramas por HU (reemplazado arriba)

- `main`: solo lo estable, lo que se entrega. Protegida: solo recibe PR desde `develop`.
- `develop`: integración y pruebas.
- `feature/HU-XX-descripcion`: una rama por HU, sale de `develop` y vuelve a `develop`.

Commits con el número de la HU (`HU-01: ...`).
