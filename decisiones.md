# Decisiones

Registro de decisiones técnicas y de producto. La más reciente va arriba.

## 2026-11-22 — Cierre: ramas protegidas y una sola dirección pública

- **Ramas protegidas en los dos repos:** `main` y `dev` solo aceptan cambios por PR, sin force push ni borrado, y la regla también aplica a los administradores. En lista-tareas además se exige el CI ("test") en verde.
- **Sincronizar `dev` después de una entrega:** como `dev` está protegida, ya no se sube directo. Se hace con un PR `main → dev` (back-merge).
- **Ramas:** se borraron las ramas `chore/` ya unidas (los PR conservan su historial). Las `huN` se mantienen como historial por HU.
- **GitHub Pages de la app apagado:** la única dirección de la app es la de Vercel. El tablero de este repo sigue en GitHub Pages.

## 2026-11-22 — Despliegue con Vercel (reemplaza GitHub Pages)

- La app se despliega con **Vercel**, igual que el otro proyecto del equipo. Producción: https://lista-tareas-sage.vercel.app/ (rama `main`).
- Vercel está conectado al repositorio de GitHub. Cada merge a `main` publica en producción y cada PR genera una vista previa, protegida con el inicio de sesión de Vercel.
- `vercel.json` (lista-tareas#22): build de Vite hacia `dist`, cabeceras de seguridad (CSP que solo permite Google Fonts como origen externo, `nosniff`, `X-Frame-Options: DENY`, HSTS, `Referrer-Policy`, `Permissions-Policy`) y caché inmutable para `/assets/`.
- Se quitó el workflow de GitHub Pages. La v1.1.1 se había publicado por error en GitHub Pages; esa dirección queda obsoleta.

## 2026-11-22 — Finales de línea LF y plantilla de PR

- `.gitattributes` con `* text=auto eol=lf` en los dos repos. En Windows, `core.autocrlf=true` mezclaba CRLF y LF en los archivos editados. Ahora el repo fija LF para todos.
- Plantilla `.github/pull_request_template.md` con la lista de verificación de cada HU (criterios, pruebas, navegador, Figma y documentación) en lista-tareas, y la de documentación en este repo.

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
