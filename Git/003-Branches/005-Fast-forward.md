# Fast-forward

Un **Fast-forward** es una forma de hacer un `merge` cuando **la rama que recibe los cambios no tiene ningún commit nuevo desde que se creó la otra rama**.

Git no necesita crear un commit adicional porque simplemente puede **mover la referencia de la rama hacia adelante**.

Por ejemplo:

```
A → B → C
         ↑
        main
```

Creas `desarrollo` desde `C` y haces dos commits:

```
A → B → C → D → E
         ↑       ↑
        main   desarrollo
```

Si ahora haces:

```
git switch main
git merge desarrollo
```

Git puede mover `main` directamente hasta `E`:

```
A → B → C → D → E
                 ↑
             main
             desarrollo
```

No se crea un nuevo commit de merge porque **no hay dos líneas de desarrollo que realmente tengan que combinarse**. `main` simplemente estaba detrás de `desarrollo`.

Por eso se llama **Fast-forward**: Git puede avanzar la referencia de la rama directamente hasta el commit más reciente.