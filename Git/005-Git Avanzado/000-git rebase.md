# `git rebase`

`git rebase` sirve para **recolocar los commits de una rama sobre otra base**, modificando la forma en la que aparece el historial.

A diferencia de `merge`, que une dos líneas de desarrollo, `rebase` **reconstruye los commits de una rama como si hubieran sido creados partiendo de otro commit**.

Por ejemplo, tienes:

```
A → B → C
     \
      D → E
```

`main` avanzó hasta `C` y tu rama de trabajo tiene `D` y `E`.

Si haces un rebase de tu rama sobre `main`, Git toma `D` y `E` y los vuelve a aplicar sobre `C`:

```
A → B → C → D' → E'
```

Los commits `D'` y `E'` son **nuevos commits**, aunque contengan los mismos cambios que `D` y `E`. Por eso sus hashes serán diferentes.

La diferencia fundamental es:

```
merge
→ une dos historiales
→ puede crear un merge commit

rebase
→ cambia la base de una rama
→ reconstruye sus commits
→ produce un historial más lineal
```

El rebase es muy útil para mantener un historial limpio, pero hay que tener cuidado porque **reescribe el historial**. Por eso no conviene hacer rebase de commits que otras personas ya estén utilizando como parte de una rama compartida.