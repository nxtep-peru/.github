# Tableros de proyecto

Cada proyecto de Nxtep lleva su trabajo en un tablero de GitHub Projects,
y todos salen de la misma plantilla de la organización: **Project
Template**. Así el flujo, los campos y las vistas son iguales en todos, y
quien pasa de un proyecto a otro no tiene que aprender un tablero nuevo.

## Qué trae la plantilla

**Flujo.** El campo `Status` tiene cinco estados: `Backlog`,
`In progress`, `In review`, `Blocked` y `Done`. Los dos primeros saltos,
a `In progress` al abrir la rama y a `In review` al abrir el PR, los hace
una persona. A `Done` lo lleva GitHub cuando se cierra el issue o se
mergea su PR, y por eso todo PR que resuelve un issue lleva `Closes #N`
en el cuerpo.

**Campos.**

| Campo | Qué dice |
|---|---|
| `Type` | Bug, Feature o Task, según el formulario con que se abrió el issue |
| `Frente` | Qué clase de trabajo es. Parte con Backend, Frontend, IA, Datos, DevOps y Producto, y cada proyecto ajusta las opciones |
| `Priority` | Qué tan importante es ahora |
| `Effort` | Cuánto trabajo lleva, estimado antes de empezar |
| `Start date`, `Target date` | Las fechas de una épica, que dibujan el Roadmap |

`Priority`, `Effort`, `Start date` y `Target date` son campos de la
organización: viven en el issue y se ven igual en cualquier tablero.

**Vistas.** Backlog (el tablero por estado), Priority board, Team items,
Frentes, Roadmap y My items, que muestra lo asignado a quien la mira.

**Automatizaciones.** Suman al tablero los sub-issues de lo que ya está
en él y mueven las tarjetas cuando se enlaza un PR, cuando se mergea y
cuando se cierra el issue.

**README.** Las reglas del tablero: el flujo, cuándo se llena cada campo,
cómo se cierra el trabajo de DevOps y la pasada semanal de diez minutos.

## Crear el tablero de un proyecto nuevo

1. En la organización, **Projects → New project**, y elige **Project
   Template** entre las plantillas.
2. Ponle el nombre del proyecto y una descripción corta.
3. Copia el README de la plantilla: GitHub no lo copia solo.
4. Ajusta las opciones de `Frente` a los frentes del proyecto, y esa
   misma lista en el README.
5. En **Workflows**, activa **Auto-add to project** apuntando al repo del
   proyecto. La plantilla no copia esta automatización, y en el plan
   gratuito hay una sola por tablero, que cubre un solo repo.
6. En **Settings → Manage access**, da acceso de escritura al team del
   proyecto.

## Cambiar la plantilla

Un cambio de flujo, de campos o de vistas se hace primero en **Project
Template** y después en los tableros que ya existen, porque un tablero
creado desde la plantilla no se actualiza solo. Si el cambio toca estas
reglas, este documento se actualiza en el mismo PR.
