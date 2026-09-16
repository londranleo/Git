# Git revert

`git revert` sirve para **deshacer los cambios introducidos por un commit creando un nuevo commit**.

Esto es diferente de `git reset`.

Supongamos que tienes:

```
A → B → C
```

El commit `C` contiene un cambio que provocó un problema. Si haces:

```
git revert C
```

Git crea un nuevo commit:

```
A → B → C → D
```

El commit `D` **invierte los cambios que había realizado `C`**, pero `C` sigue existiendo en el historial.

Por ejemplo:

```
git commit -m "Añadir login"
git commit -m "Añadir sistema de pagos"
```

Si el sistema de pagos tiene un problema:

```
git revert <commit-del-sistema-de-pagos>
```

Git crea otro commit que deshace ese sistema.

La diferencia fundamental es:

```
git reset
→ mueve la referencia del historial hacia atrás

git revert
→ conserva el historial y crea un nuevo commit que deshace otro
```

Por eso `git revert` es especialmente útil cuando **el historial ya ha sido compartido con otras personas o subido a GitHub**, porque no necesitas eliminar ni reescribir los commits existentes.