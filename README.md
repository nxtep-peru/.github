# .github

La configuración por defecto de GitHub para los repos de `nxtep-peru`.
GitHub la aplica a todo repo que no tenga la suya.

| Archivo | Qué hace |
|---|---|
| `profile/README.md` | La portada de [github.com/nxtep-peru](https://github.com/nxtep-peru) |
| `.github/ISSUE_TEMPLATE/` | Los formularios de issue, uno por tipo: Bug, Feature y Task |
| `.github/pull_request_template.md` | La plantilla de los pull requests |
| `CONTRIBUTING.md` | Cómo se trabaja en todos los repos |
| `docs/projects.md` | Cómo funcionan los tableros de proyecto y cómo se crea uno nuevo desde **Project Template** |
| `SECURITY.md` | Cómo reportar una vulnerabilidad |

Un repo que define su propia carpeta `.github/ISSUE_TEMPLATE` deja de
usar **todos** los formularios de aquí, no solo los que reemplaza.

La tabla de proyectos de `profile/README.md` se actualiza a mano: cuando
un proyecto cambia de etapa o nace uno nuevo, se corrige en un PR, junto
con la fecha del estado.

Este repo es público porque GitHub lo exige para aplicar las plantillas.
Aquí no va nada interno.
