# Configuración Inicial (Genaro)

**Objetivo:** Crear ramas y configurar el repositorio para el workflow.

## Crear rama `dev` desde `main`

```bash
git checkout main          # Cambiar a la rama main
git pull origin main       # Actualizar main con la versión remota
git checkout -b dev        # Crear y cambiar a la rama dev
git push -u origin dev     # Subir rama dev a GitHub
```

- `git checkout main`: Se cambia a la rama principal `main`.
- `git pull origin main`: Descarga los últimos cambios de la rama `main` remota (en GitHub) y los fusiona con la rama `main` local.
- `git checkout -b dev`: Crea una nueva rama llamada `dev` a partir de la rama actual (`main`) y se cambia a esa nueva rama.
- `git push -u origin dev`: Sube la rama `dev` al repositorio remoto (en GitHub) y la configura para que haga seguimiento de la rama remota `origin/dev`.

## Crear ramas para colaboradores (basadas en `dev`)

```bash
git checkout dev           # Asegurarse de estar en dev
git checkout -b genaro     # Crear rama genaro
git push -u origin genaro  # Subir a GitHub
git checkout dev           # Volver a dev
git checkout -b gonzalo    # Crear rama gonzalo
git push -u origin gonzalo
git checkout dev
git checkout -b limberth   # Crear rama limberth
git push -u origin limberth
```

- `git checkout dev`: Se asegura de estar en la rama `dev`.
- `git checkout -b <nombre_rama>`: Crea una nueva rama con el nombre especificado a partir de la rama actual (`dev`) y se cambia a esa nueva rama.
- `git push -u origin <nombre_rama>`: Sube la rama al repositorio remoto y la configura para seguimiento.

## Proteger ramas críticas (en GitHub)

1. Ir a **Settings → Branches** en el repositorio de GitHub.
2. Proteger `main`:
    - **Require a pull request before merging:** Activar.
    - **Require approvals:** 1 (Genaro como aprobador).
3. Proteger `dev`:
    - **Require a pull request before merging:** Activar.
    - **Require approvals:** 1 (Genaro como aprobador).