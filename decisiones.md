# Decisiones

Registro de decisiones técnicas y de producto. La más reciente va arriba.

## 2026-11-22 — Eliminar sin confirmación

Al pulsar eliminar, la tarea se borra de inmediato, sin diálogo ni "deshacer". Es una lista personal y simple. Se puede revisar si resulta molesto.

## 2026-11-22 — Agregar deshabilitado con el campo vacío

El botón **Agregar** se deshabilita mientras no haya texto, para evitar tareas en blanco sin mostrar mensajes de error.

## 2026-11-22 — Diseño en Figma

El diseño se hace en Figma y es la fuente de verdad. Los tokens de Figma se pasan al código como variables CSS. Ver [diseno.md](diseno.md).

## 2026-11-22 — Stack: Vite + JavaScript + Vitest

App web sin framework, con Vite para desarrollo y build, y Vitest para pruebas. Es lo más simple para una lista de tareas en el navegador. El CI (GitHub Actions) ejecuta pruebas y build en cada PR.

## 2026-11-22 — Flujo de ramas por HU

- `main`: solo lo estable, lo que se entrega. Protegida: solo recibe PR desde `develop`.
- `develop`: integración y pruebas.
- `feature/HU-XX-descripcion`: una rama por HU, sale de `develop` y vuelve a `develop`.

Commits con el número de la HU (`HU-01: ...`). Este repo de documentación sigue el mismo flujo.
