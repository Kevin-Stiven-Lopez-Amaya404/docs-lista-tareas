# ADR-003: Botón Agregar deshabilitado con el campo vacío

**Estado:** ACCEPTED
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** HU-01

---

## Contexto

Hay que evitar tareas en blanco.

## Decisión

Se decide **deshabilitar el botón Agregar** mientras el campo esté vacío o solo tenga espacios, en lugar de mostrar mensajes de error. La lógica además ignora textos vacíos (`agregarTarea` y `editarTarea` hacen `trim()`).

## Consecuencias

### Positivas

- Sin mensajes de error que leer ni que traducir.

### Negativas / Trade-offs

- No se explica por qué el botón está deshabilitado; se confía en que el campo vacío es evidente.

## Alternativas consideradas

| Alternativa | Por qué se descartó |
|-------------|---------------------|
| Mensaje de validación al enviar | Más interfaz para un caso que se puede evitar de antemano |

## Referencias

- Registro original: [99-archive/old-decisions/decisiones.md](../../../99-archive/old-decisions/decisiones.md)
