# Recuperar cambios o commits perdidos

Git permite recuperar ciertos cambios o commits que parecen haber desaparecido. Esto es posible porque Git conserva referencias y movimientos anteriores durante un tiempo, y aquí es donde `git reflog` resulta especialmente útil.

Por ejemplo, tienes:

```
A → B → C
```

y haces:

```
git reset --hard B
```

Ahora tu rama está en:

```
A → B
```

El commit `C` ya no aparece en el historial normal de la rama, por lo que podría parecer que lo has perdido.

Pero puedes consultar:

```
git reflog
```

y encontrar el estado anterior:

```
HEAD@{0} → B
HEAD@{1} → C
```

Si identificas el hash de `C`, puedes volver a él:

```
git reset --hard <hash-de-C>
```

También puedes crear una rama desde ese commit si quieres conservarlo sin mover tu rama actual:

```
git switch -c recuperado <hash-de-C>
```

Esto es precisamente una de las razones por las que `git reflog` es tan importante: **un commit que ha dejado de estar referenciado por una rama no necesariamente ha desaparecido inmediatamente del repositorio**.

Hay que distinguir esto de `git restore`: `restore` está pensado principalmente para descartar o recuperar cambios de archivos, mientras que `reflog` permite localizar estados anteriores de las referencias y recuperar commits que ya no están en el historial visible.