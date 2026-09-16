# `git stash`

`git stash` sirve para **guardar temporalmente cambios que tienes en tu directorio de trabajo sin crear un commit**.

Es útil cuando estás trabajando en algo que todavía **no está terminado**, pero necesitas cambiar de rama o trabajar en otra cosa.

Cuando haces:

```
git stash
```

Git guarda temporalmente tus cambios y deja tu directorio de trabajo limpio.

Después puedes recuperar esos cambios con:

```
git stash pop
```

`stash` **no crea un commit** y tampoco elimina definitivamente tus cambios. Los guarda en una zona temporal administrada por Git.

Puedes tener varios `stash` al mismo tiempo. Para verlos:

```
git stash list
```

Por ejemplo:

```
stash@{0}: WIP en sistema de login
stash@{1}: WIP en documentación
```

Y puedes recuperar uno concreto:

```
git stash apply stash@{0}
```

La diferencia principal es:

```
git commit
→ guarda el trabajo como parte permanente del historial

git stash
→ guarda temporalmente trabajo que todavía no quieres convertir en commit
```