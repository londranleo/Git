# Referencias y hashes

En Git, un **hash** identifica de forma única a un objeto, como un commit. Por ejemplo:

```
a82f31c9e4...
```

Cuando haces:

```
git log --oneline
```

puedes ver algo como:

```
a82f31c Añadir login
7bc921c Añadir usuarios
31d4aa2 Crear proyecto
```

El hash permite decirle a Git **exactamente a qué commit te estás refiriendo**:

```
git show a82f31c
```

Una **referencia**, en cambio, es un nombre que Git utiliza para apuntar a un commit. Por ejemplo, una rama como `main` es una referencia:

```
main
 ↓
C
```

En lugar de tener que escribir continuamente el hash del commit actual, puedes utilizar:

```
main
HEAD
HEAD~1
```

Por ejemplo:

```
A ← B ← C
        ↑
       main
        ↑
       HEAD
```

Aquí:

- `main` apunta a `C`.
- `HEAD` indica que estás trabajando actualmente sobre `main`.
- El hash de `C` identifica directamente ese commit.
- `HEAD~1` se refiere a `B`.

La diferencia fundamental es que **el hash identifica directamente un commit**, mientras que **una referencia es un nombre que apunta a un commit y puede cambiar con el tiempo**.

Por ejemplo, si creas un nuevo commit:

```
A ← B ← C ← D
            ↑
           main
```

El hash de `C` sigue siendo el mismo, pero la referencia `main` ahora apunta a `D`.