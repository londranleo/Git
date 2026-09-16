# Git merge 

`git merge` permite **integrar en una rama los cambios que existen en otra rama**.

Una rama representa una línea independiente de desarrollo. Cuando trabajas en una rama secundaria, sus commits no aparecen automáticamente en otra rama.

`merge` es el mecanismo que permite unir esas líneas de desarrollo.

Lo importante es entender **desde qué rama ejecutas el comando**. La rama en la que estás situado es la que **recibirá** los cambios.

Por ejemplo, si estás trabajando en `main` y quieres incorporar lo que has desarrollado en `desarrollo`:

```
git switch main
git merge desarrollo
```

Git toma los cambios que existen en `desarrollo` y los integra en `main`.

Dependiendo de cómo sean las dos ramas, Git puede realizar la integración de diferentes formas. 