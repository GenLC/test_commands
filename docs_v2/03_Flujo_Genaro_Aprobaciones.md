# Flujo diario para Genaro (dueño del proyecto)

**Objetivo:** Revisar cambios, aprobar PRs y mantener `main` estable.

## Revisar Pull Requests (PRs)

1. En GitHub, ir a **Pull Requests**.
2. Revisar cada PR (de `genaro`, `gonzalo` o `limberth` a `dev`):
    - Ver cambios en **Files changed**.
    - Aprobar o solicitar correcciones.

## Aprobar y fusionar PRs a `dev`

Si el PR está OK:

1. Hacer clic en **Merge Pull Request**.
2. Confirmar fusión.
3. Eliminar rama (opcional) si ya no se usará.

## Probar cambios en `dev`

Actualizar `dev` local:

```bash
git checkout dev
git pull origin dev        # Traer cambios fusionados
```

- `git checkout dev`: Cambia a la rama `dev`.
- `git pull origin dev`: Descarga los últimos cambios de la rama `dev` remota y los fusiona con la rama `dev` local.

## Actualizar `main` desde `dev`

1. Crear PR de `dev` a `main`:
    - En GitHub: **New Pull Request → Base: `main`, Compare: `dev`**.
2. Aprobar y fusionar.

```bash
git checkout main
git pull origin main
```
-   `git checkout main`: Cambia a la rama `main`.
-   `git pull origin main`: Descarga y fusiona (actualiza) la rama local `main` con la rama remota `main`.

Siempre actualizar tu rama con `dev` antes de trabajar:

```bash
git checkout tu-rama
git merge dev
```
- `git checkout tu-rama`: Cambia a tu rama de trabajo.
- `git merge dev`: Fusiona los cambios de `dev` en tu rama de trabajo.

## Revertir un PR en `dev`

```bash
# Supongamos que el commit problemático es a1b2c3d
git checkout dev
git pull origin dev
git revert a1b2c3d
git push origin dev
```

- `git checkout dev`: Cambia a la rama `dev`.
- `git pull origin dev`: Actualiza la rama `dev` local.
- `git revert a1b2c3d`: Revierte el commit especificado (crea un nuevo commit que deshace los cambios).
- `git push origin dev`: Sube el commit de reversión al repositorio remoto.