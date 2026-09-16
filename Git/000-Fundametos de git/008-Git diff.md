# Git diff
`git diff` sirve para **ver exactamente qué ha cambiado en tus archivos desde el último estado registrado**.

Por ejemplo, Git ya tiene guardado:

```
Main.java
```

y después modificas el archivo:

```
System.out.println("Hola");
```

Si ejecutas:

```
git diff
```

Git compara el contenido que tienes actualmente con el contenido que estaba registrado y te muestra las diferencias.

Por ejemplo:

```
- System.out.println("Hola");
+ System.out.println("Hola mundo");
```

El `-` representa lo que estaba antes y el `+` lo que tienes ahora.

Esto es especialmente útil cuando has hecho muchos cambios y quieres revisar **qué modificaste antes de hacer `git add` y `git commit`**.

También existe:

```
git diff --staged
```

que muestra las diferencias de los cambios que **ya están en la Staging Area**, es decir, después de hacer `git add`.

Por ahora, la diferencia importante es:

```
git diff
        → cambios que todavía NO están en staging

git diff --staged
        → cambios que YA están en staging
```