# HU-06: Guardar tareas al cerrar el navegador

| | |
|---|---|
| **Estado** | Entregado en v1.0.0 (2026-11-22) |
| **Rama** | `hu6` |
| **PR** | [lista-tareas#9](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas/pull/9) |
| **Diseño** | No tiene interfaz |

## Historia

Como **usuario**, quiero **que mis tareas sigan ahí cuando vuelva a abrir la página** para **no perderlas**.

## Criterios de aceptación

- [x] Las tareas (texto y estado) se guardan en el navegador (`localStorage`) cada vez que cambian.
- [x] Al abrir la página, se cargan las tareas guardadas.
- [x] Si los datos guardados están dañados o el navegador no permite guardar, la app abre con la lista vacía y sigue funcionando.

## Implementación

- **Módulo:** `src/almacenamiento.js` con `cargarTareas()` y `guardarTareas()` sobre `localStorage`, clave `lista-tareas:v1` (el `v1` permite migrar el formato en el futuro).
- **Datos no confiables:** si lo guardado es JSON dañado, no es una lista o el almacenamiento está bloqueado, se empieza con la lista vacía. Las tareas inválidas (sin id de texto, texto vacío, sin estado) se descartan y solo se conservan `id`, `texto` y `completada`. Si no se puede guardar (sin espacio o bloqueado), la app sigue funcionando en memoria.
- **Interfaz:** en `src/main.js` todos los cambios de la lista pasan por `actualizar()`, que guarda. Así ninguna acción nueva puede olvidar guardar. El estado de edición no se guarda.
- **Pruebas:** 5 nuevas en `src/almacenamiento.test.js` con un almacenamiento falso (guardar y cargar, vacío, dañado, tareas inválidas, almacenamiento bloqueado): 23 en total. Verificado en el navegador: agregar, editar, completar y eliminar, recargar y comprobar que todo se conserva; con datos dañados abre vacía y se puede seguir agregando.
