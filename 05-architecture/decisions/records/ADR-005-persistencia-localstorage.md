# ADR-005: Persistencia en localStorage con validación

**Estado:** ACCEPTED
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** HU-06

---

## Contexto

Las tareas deben sobrevivir a recargar o cerrar el navegador, sin servidor.

## Decisión

Se decide guardar en **`localStorage`** con la clave versionada `lista-tareas:v1` (`src/almacenamiento.js`). Lo guardado se trata como **no confiable**: se descartan los elementos inválidos y, si el JSON está dañado o el navegador bloquea el almacenamiento, la app arranca vacía y sigue funcionando en memoria. Detalle en [06-data/models.md](../../../06-data/models.md).

## Consecuencias

### Positivas

- Sin backend, sin cuentas y sin coste.
- El `v1` de la clave permite migrar el formato más adelante.

### Negativas / Trade-offs

- Las tareas no se sincronizan entre dispositivos ni navegadores.
- Borrar los datos del sitio borra las tareas.

## Alternativas consideradas

| Alternativa | Por qué se descartó |
|-------------|---------------------|
| Backend con base de datos | Fuera del alcance de una lista personal (ver [alcance](../../../01-context/scope.md)) |

## Referencias

- Historia: [HU-06](../../../04-requirements/user-stories.md#hu-06)
