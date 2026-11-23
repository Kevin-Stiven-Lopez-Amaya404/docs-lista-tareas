# Guía de contribución

Este repositorio documenta lo que se construye en [lista-tareas](https://github.com/Kevin-Stiven-Lopez-Amaya404/lista-tareas), HU por HU.

## Regla de oro

No trabajar directamente sobre `dev` ni `main` (están protegidas). Todo cambio entra por una rama `docs/tema` (o `chore/…`) y un Pull Request a `dev`. La documentación **no se trabaja por HU**: se actualizan las secciones que correspondan.

## Estructura general

| Sección | Propósito |
|---------|-----------|
| `00-governance/` | Reglas del repositorio documental |
| `01-context/` | Contexto, alcance y glosario |
| `02-domain/` | Entidad Tarea y reglas de negocio |
| `03-product/` | Visión, roadmap y backlog |
| `04-requirements/` | Requisitos, HU y trazabilidad |
| `05-architecture/` | Arquitectura y ADRs |
| `06-data/` | Modelo de datos |
| `07-api/` | No aplica (sin API) |
| `08-uml/` | Diagramas |
| `09-microservices/` | No aplica (sin servicios) |
| `10-devops/` | Setup, CI/CD y entornos |
| `11-quality/` | Pruebas y revisión |
| `12-ux-ui/` | Design system |
| `13-operations/` | No aplica (sin servidor propio) |
| `14-training/` | Manuales |
| `15-project-control/` | Riesgos y preguntas abiertas |
| `16-technical-manuals/` | Manuales técnicos |
| `99-archive/` | Documentos reemplazados |

El `README.md` de cada carpeta es el índice de esa sección.

## Flujo rápido

1. Identifica la sección correcta según la tabla.
2. Revisa [documentation-rules.md](./00-governance/documentation-rules.md).
3. Crea la rama según [git-conventions.md](./00-governance/git-conventions.md): `docs/tema` (por ejemplo `docs/requisitos-hu11`).
4. Edita o crea el documento con la cabecera de estado, fecha y autor.
5. Registra el archivo en el `README.md` de su sección.
6. Abre el PR a `dev` y completa la plantilla.

## Agregar una HU

1. Copia el bloque de [04-requirements/_template-hu.md](./04-requirements/_template-hu.md) al final de [user-stories.md](./04-requirements/user-stories.md) y añade su fila en la tabla del inicio.
2. Añádela a la [matriz de trazabilidad](./04-requirements/traceability-matrix.md) con su requisito.
3. Actualiza la tarjeta del tablero (`index.html`).
4. Sigue la [matriz de touchpoints](./00-governance/docs-touchpoints-matrix.md) para el resto.

## Agregar una decisión

Copia [05-architecture/decisions/_template-adr.md](./05-architecture/decisions/_template-adr.md) con el siguiente número libre y regístrala en [records/README.md](./05-architecture/decisions/records/README.md).
