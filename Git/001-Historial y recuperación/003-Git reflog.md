# Git reflog

`git reflog` sirve para **ver el historial de movimientos de `HEAD` y de las referencias de tu repositorio**, incluso cuando un commit ya no aparece en `git log`.

Esto es especialmente útil para **recuperar commits o estados que aparentemente has perdido**.

Por ejemplo, tienes:

```
A → B → C
```

Haces:

```
git reset --hard B
```

Ahora `git log` mostrará:

```
A → B
```

Parece que `C` desapareció. Sin embargo, Git puede conservar la referencia de que `HEAD` estuvo anteriormente en `C`.

Si ejecutas:

```
git reflog
```

puedes encontrar algo parecido a:

```
b82c31 HEAD@{0}: reset: moving to B
a91d52 HEAD@{1}: commit: Añadir login
```

Entonces puedes utilizar ese identificador para volver a ese estado.

La diferencia importante es:

```
git log
→ historial de commits de la rama

git reflog
→ historial de dónde han estado HEAD y las referencias
```

`reflog` es principalmente una **herramienta de recuperación**. No es un historial que normalmente compartas con otras personas, y su información es local a tu repositorio.