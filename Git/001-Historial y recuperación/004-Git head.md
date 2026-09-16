# Git head

`HEAD` es una **referencia que indica en qué punto del historial estás trabajando actualmente**.

Por ejemplo, si tienes:

```
A → B → C
```

y actualmente estás en `C`, conceptualmente tienes:

```
A → B → C
         ↑
        HEAD
```

Cuando creas un nuevo commit `D`:

```
A → B → C → D
             ↑
            HEAD
```

`HEAD` normalmente apunta a la **rama actual**, y esa rama apunta al commit en el que estás.

Por ejemplo:

```
HEAD
 ↓
main
 ↓
C
```

Por eso, cuando haces:

```
git commit
```

Git crea el nuevo commit a partir del estado al que apunta `HEAD` y actualiza la referencia correspondiente.

También puedes utilizar `HEAD` en comandos para referirte al commit actual:

```
git show HEAD
```

muestra el commit actual.

Y:

```
git diff HEAD
```

compara tus cambios actuales con el commit al que apunta `HEAD`.

Más adelante veremos expresiones como:

```
HEAD~1
HEAD~2
```

que permiten referirse a commits anteriores respecto al punto actual.