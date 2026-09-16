# Git switch

`git switch` sirve para **cambiar de una rama a otra**.

Por ejemplo, tienes:

```
main
prueba
```

y actualmente estás en `main`:

```
* main
  prueba
```

Puedes cambiar a `prueba` con:

```
git switch prueba
```

Ahora:

```
  main
* prueba
```

A partir de ese momento, los nuevos commits que hagas se crearán sobre la rama `prueba`.

También puedes crear una rama **y cambiarte a ella en un solo comando**:

```
git switch -c desarrollo
```

Esto equivale a:

```
git branch desarrollo
git switch desarrollo
```

La diferencia es importante:

```
git branch prueba
→ crea la rama, pero te quedas donde estabas

git switch prueba
→ cambia a una rama que ya existe

git switch -c prueba
→ crea la rama y cambia a ella
```

`git switch` está pensado específicamente para **cambiar entre ramas**, mientras que `git branch` se utiliza principalmente para **gestionar las ramas**.