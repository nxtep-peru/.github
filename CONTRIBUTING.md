# Cómo trabajamos

Esto vale para todos los repos de Nxtep. Lo propio de cada uno, como
levantarlo o sus scopes de commit, está en su README.

## Issues

Todo trabajo empieza en un issue, abierto con el formulario de su tipo:

| Tipo | Para qué |
|---|---|
| **Bug** | Algo no funciona como debería |
| **Feature** | Algo nuevo o distinto que podrá hacer quien usa el producto |
| **Task** | El resto: configuración, refactor, dependencias, documentación, diseño o investigación |

- Un issue por cosa. Si es grande, se parte en sub-issues.
- Quien lo toma se asigna en **Assignees**; su nombre no va en el título.
- La prioridad y el esfuerzo van en los campos **Priority** y **Effort**,
  y se completan al planificar.
- Nada de secretos en un issue: ni contraseñas, ni tokens, ni datos
  personales.

## Ramas

Trabajamos con ramas cortas sobre `main` (trunk-based). Nada se commitea
ni se empuja directo a `main`: todo entra por pull request, aunque sea
una línea.

La rama usa el mismo vocabulario que el commit, en minúsculas y
kebab-case:

```
tipo/descripcion-corta
```

Por ejemplo, `feat/cors-allowed-origins` o `docs/skills-backend`. Una
rama vive horas o días; si pasa de una semana, el cambio debió partirse.

## Commits

Usamos [Conventional Commits](https://www.conventionalcommits.org/es/v1.0.0/),
con scope y la descripción en español:

```
tipo(scope): descripción en minúscula y sin punto final
```

- Los tipos son los de Conventional Commits: `feat`, `fix`, `docs`,
  `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore` y `revert`.
- Los scopes cambian de un repo a otro, y la lista está en el validador
  de commits de cada repo (`.githooks/commit-msg` o
  `commitlint.config.*`).
- Cada commit tiene un solo autor: quien lo propone.

## Pull requests

- **El título es el de un commit**, porque el PR se integra con squash
  merge y el título queda tal cual en `main`.
- **El cuerpo empieza por el porqué**: qué problema había y qué pasaba
  si nadie lo tocaba. Después, solo lo que aplique: qué cambia, qué no
  cambia y qué falta por verificar. La plantilla trae esa estructura.
- **Si resuelve un issue**, la última línea es `Closes #123`, y GitHub
  lo cierra al mergear.
- Se integra con el botón **Squash and merge** de GitHub, y la rama se
  borra sola.

## Asistentes de IA

Programamos con asistentes de IA, como Claude Code, sobre una
configuración compartida que impide lo que no debe pasar: commitear o
empujar directo a `main`, forzar un push o leer un archivo `.env`. Lo que
escribe un asistente pasa por la misma revisión que lo que escribe una
persona, y lo firma quien lo propone, que responde por el cambio. Por eso
ni los commits ni los PR llevan atribución de herramientas.

## Secretos

Ningún secreto entra en git. Cada repo documenta sus variables en un
`.env.example`, y los valores reales se piden al lead del proyecto por un
canal privado.

## Nombres

Repos, archivos y carpetas, en inglés; los textos, en español. Cada repo
se llama `<proyecto>-NN-<rol>`, por ejemplo `<proyecto>-01-backend`, y lo
que es transversal a la organización pertenece al proyecto `platform`.
