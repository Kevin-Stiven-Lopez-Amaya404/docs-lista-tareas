# Modelo de datos

> Estado: 🟢 Estable | Última actualización: 2026-11-23
> Autor: Kevin-Stiven-Lopez-Amaya404 | Equipo: lista-tareas
## Almacenamiento

| Campo | Valor |
|-------|-------|
| Dónde | `localStorage` del navegador |
| Clave | `lista-tareas:v1` |
| Formato | JSON: arreglo de tareas |
| Código | `src/almacenamiento.js` (`cargarTareas`, `guardarTareas`) |

```json
[
  { "id": "3f1c…", "texto": "Comprar pan", "completada": false },
  { "id": "9a2b…", "texto": "Llamar al banco", "completada": true }
]
```

## Validación al cargar

Un elemento se conserva solo si `id` es texto, `texto` es texto no vacío y `completada` es booleano. Se guardan solo esos tres campos. Si el JSON está dañado, no es un arreglo o el navegador bloquea el acceso, se carga una lista vacía.

## Al guardar

Se guarda en cada cambio. Si falla (sin espacio o bloqueado), la app sigue en memoria sin mostrar error.

## Versionado

El sufijo `v1` permite cambiar el formato en el futuro: una versión nueva usaría `lista-tareas:v2` y migraría desde `v1` al cargar. Desde v1.0.0 el formato no ha cambiado.
