# Git branch 

`git branch` sirve para **crear, consultar, cambiar el nombre y eliminar ramas**.

Si ejecutas:

```bash
git branch
```

Git muestra las ramas locales que existen:

```bash
* main
  prueba
  desarrollo
```

El `*` indica **la rama en la que estás actualmente**.

Para crear una rama:

```
git branch prueba
```

Esto crea `prueba`, pero **no cambia tu rama actual**.

Por ejemplo, si estabas en `main`:

```
main
  ↑
 HEAD
```

después de:

```
git branch prueba
```

tienes:

```
main
prueba
  ↑
 HEAD
```

Sigues estando en `main`.

También puedes eliminar una rama local:

```
git branch -d prueba
```

Y cambiar el nombre de la rama actual:

```
git branch -M main
```

Por tanto, `git branch` se centra en **gestionar las ramas**, mientras que el cambio de una rama a otra lo veremos con `git switch`.