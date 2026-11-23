# ADR-004: Eliminar sin confirmación

**Estado:** ACCEPTED
**Fecha:** 2026-11-22
**Autores:** Kevin-Stiven-Lopez-Amaya404
**HU relacionada:** HU-05, HU-10

---

## Contexto

Al eliminar una tarea se puede pedir confirmación, ofrecer deshacer o borrar directamente.

## Decisión

Se decide que **la tarea se borra de inmediato**, sin diálogo ni "deshacer". Es una lista personal y simple. La HU-10 (borrar completadas) sigue el mismo criterio.

## Consecuencias

### Positivas

- Menos pasos para el usuario.

### Negativas / Trade-offs

- Un clic por error borra la tarea sin forma de recuperarla.

## Alternativas consideradas

| Alternativa | Por qué se descartó |
|-------------|---------------------|
| Diálogo de confirmación | Interrumpe una acción frecuente |
| Deshacer | Más estado y más interfaz; se puede revisar si resulta molesto |

## Referencias

- Registro original: [99-archive/old-decisions/decisiones.md](../../../99-archive/old-decisions/decisiones.md)
