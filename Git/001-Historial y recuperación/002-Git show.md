# Git show

`git show` sirve para **ver el contenido y los cambios asociados a un commit concreto**.

Mientras que:

```
git log
```

te muestra **la lista de commits**, `git show` te permite **inspeccionar uno de ellos en detalle**.

Por ejemplo:

```
git show
```

muestra información del **último commit**, incluyendo su identificador, autor, mensaje y los cambios que introdujo.

También puedes indicar un commit concreto utilizando su hash:

```
git show a82f31
```

Git mostrará ese commit y el `diff` correspondiente, es decir, qué líneas se añadieron, eliminaron o modificaron.

La diferencia entre ambos es:

```
git log
→ ¿Qué commits existen?

git show <commit>
→ ¿Qué contiene este commit y qué cambios hizo?
```

También puedes utilizarlo para consultar otros elementos de Git, pero su uso principal ahora mismo es **inspeccionar un commit concreto**.