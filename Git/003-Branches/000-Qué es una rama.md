# Qué es una rama

Una **rama (branch)** es una referencia que permite trabajar sobre una línea de desarrollo independiente dentro de un repositorio.

Una rama no es una copia completa e independiente del proyecto. Es una referencia que apunta a un commit y que puede avanzar a medida que creas nuevos commits.

Por ejemplo, inicialmente tienes:

```
A → B → C
         ↑
        main
```

Si creas una nueva rama desde `C`:

```
A → B → C
         ↑
        main
         \
          D
           ↑
         prueba
```

Ahora existen dos líneas de desarrollo:

- `main` continúa desde `C`.
- `prueba` puede crear nuevos commits sin modificar directamente `main`.

Si posteriormente haces otro commit en `prueba`:

```
A → B → C
         ↑
        main
         \
          D → E
               ↑
             prueba
```

Los commits `D` y `E` pertenecen a la línea de desarrollo de `prueba`.

Las ramas permiten, por ejemplo, desarrollar una nueva funcionalidad sin modificar directamente la rama principal del proyecto.

Cuando termines el trabajo de una rama, puedes integrar sus cambios en otra mediante `git merge`, que veremos más adelante.
