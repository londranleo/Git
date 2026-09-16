# Merge commit

Un **merge commit** aparece cuando Git necesita **unir dos líneas de desarrollo que han avanzado de forma independiente**.

A diferencia del _Fast-forward_, aquí la rama que recibe los cambios **también tiene commits nuevos** que no existen en la otra rama.

Por ejemplo:

```
        C → D
       /     \
A → B         E
       \     /
        F → G
```

`main` y `desarrollo` han evolucionado por separado.

Cuando haces:

```
git switch main
git merge desarrollo
```

Git necesita combinar ambas líneas. Para registrar esa unión puede crear un **nuevo commit de merge**:

```
        C → D ───┐
       /         ↓
A → B            M
       \         ↑
        F → G ───┘
```

`M` es el **merge commit**.

Este commit no representa necesariamente una nueva funcionalidad. Su función principal es **registrar en el historial que dos líneas de desarrollo fueron integradas**.

La diferencia con Fast-forward es:

```
Fast-forward
→ una rama simplemente avanza
→ no necesita merge commit

Merge commit
→ las dos ramas tienen historia independiente
→ Git necesita registrar la unión
```