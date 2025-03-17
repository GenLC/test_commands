# Flujo diario para colaboradores (Gonzalo y Limberth)

**Objetivo:** Trabajar en sus ramas, enviar cambios a `dev` y coordinar con Genaro.

## Actualizar rama local con `dev`

```bash
git checkout dev           # Cambiar a dev
git pull origin dev        # Traer últimos cambios de dev
git checkout gonzalo       # Cambiar a tu rama (ej: gonzalo)
git merge dev              # Integrar cambios de dev en tu rama
```

- `git checkout dev`: Cambia a la rama `dev`.
- `git pull origin dev`: Descarga los últimos cambios de la rama `dev` remota y los fusiona con la rama `dev` local.
- `git checkout gonzalo`: Cambia a la rama de trabajo personal (en este ejemplo, `gonzalo`).
- `git merge dev`: Fusiona los cambios de la rama `dev` en la rama de trabajo actual.

## Realizar cambios

- Editar archivos en tu rama.
- Guardar cambios.

## Subir cambios a GitHub

```bash
git add .                    # Preparar todos los cambios
git commit -m "Descripción del cambio"  # Ej: "Arreglo bug en login"
git push origin gonzalo      # Subir cambios a tu rama en GitHub
```

- `git add .`: Agrega todos los archivos modificados y nuevos al área de preparación (staging area).
- `git commit -m "Descripción del cambio"`: Crea un nuevo commit con los cambios preparados, incluyendo un mensaje descriptivo.
- `git push origin gonzalo`: Sube los commits de la rama local al repositorio remoto, en la rama correspondiente (en este ejemplo, `gonzalo`).

## Crear Pull Request (PR) a `dev`

1. En GitHub, ir a **Pull Requests → New Pull Request**.
2. Seleccionar:
    - **Base:** `dev` (rama destino).
    - **Compare:** Tu rama (ej: `gonzalo`).
3. Escribir descripción del cambio y @mencionar a Genaro.
4. Hacer clic en **Create Pull Request**.

## Esperar aprobación

Genaro revisará el PR. Si hay comentarios:

1. Realizar ajustes en tu rama.
2. Repetir el paso de **Subir cambios a GitHub** para actualizar el PR.

Si Genaro aprueba, el PR se fusionará a `dev`.