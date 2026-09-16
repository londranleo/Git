# Git fetch

`git fetch` sirve para **descargar desde el repositorio remoto la información nueva que existe en GitHub, sin modificar tus archivos ni tu rama actual**.

Por ejemplo, tienes:

```
GitHub
prueba: A → B → C

Tu PC
prueba: A → B
```

Si haces:

```bash
git fetch origin
```

Git descarga la información sobre `C`, pero **no incorpora `C` automáticamente a tu rama local**.

Después tendrás la información del remoto disponible:

```
GitHub
main: A → B → C
                 ↑
             origin/prueba

Tu PC
main: A → B
```

`origin/prueba` es una referencia que representa **dónde estaba la rama `main` del remoto la última vez que hiciste `fetch`**.

Esto es importante: `fetch` **no hace lo mismo que `pull`**.

```
git fetch
→ descarga información del remoto
→ no modifica tus archivos
→ no mueve tu rama actual

git pull
→ descarga información
→ además integra esos cambios en tu rama
```

En tu caso, como tienes una rama `main` en GitHub y quieres trabajar con ella, `git fetch origin` es precisamente un buen paso para **actualizar la información que tu repositorio local tiene sobre esa rama remota**.