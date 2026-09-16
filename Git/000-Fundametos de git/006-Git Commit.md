# Git Commit

`git commit` sirve para **registrar en el historial de Git los cambios que previamente has preparado en la Staging Area**.

Por ejemplo:

```
git add Main.java
```

En este momento `Main.java` está preparado, pero todavía **no forma parte de una nueva versión del historial**.

Para registrarlo:

```
git commit -m "Añadir clase Main"
```

El texto después de `-m` es el **mensaje del commit**. Sirve para describir qué cambios contiene esa versión.

El proceso hasta ahora es:

```
Modificar archivos
       ↓
    git add
       ↓
 Staging Area
       ↓
   git commit
       ↓
Historial de Git
```

Un commit representa un **punto concreto del proyecto que queda registrado en el historial**. Cada commit tiene un identificador propio, por lo que Git puede distinguirlo de los demás.

Por ejemplo:

```
A1 → Crear proyecto
B2 → Añadir usuarios
C3 → Conectar MySQL
D4 → Corregir login
```

El commit **no sube nada a GitHub**. Eso lo veremos posteriormente con `git push`.