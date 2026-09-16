# Git HEAD-1 HEAD-2

Una vez entendido `HEAD`, puedes utilizarlo para **referirte a commits anteriores sin tener que escribir su hash**.

Si tienes:

```
A → B → C → D
         ↑
        HEAD
```

Entonces:

```
HEAD
```

se refiere a `D`, el commit actual.

```
HEAD~1
```

se refiere al commit anterior:

```
A → B → C → D
         ↑
       HEAD~1
             ↑
            HEAD
```

```
HEAD~2
```

se refiere a dos commits antes:

```
A → B → C → D
     ↑       ↑
   HEAD~2   HEAD
```

Y así sucesivamente:

```
HEAD~1 → un commit atrás
HEAD~2 → dos commits atrás
HEAD~3 → tres commits atrás
```

Esto resulta útil en comandos como:

```
git show HEAD~1
```

para consultar el commit anterior, o:

```
git reset --hard HEAD~1
```

para mover la rama un commit hacia atrás.

El número indica **cuántos commits tienes que retroceder desde `HEAD`**.