# Git status

`git status` muestra **el estado actual del repositorio**.

Después de ejecutar `git init`, Git ya puede detectar qué ocurre con los archivos de tu proyecto, pero **no guarda automáticamente los cambios**.

Por ejemplo, creas:

```
MiProyecto/
├── .git/
└── Main.java
```

Ejecutas:

```
git status
```

Git puede mostrar:

```
Untracked files:
    Main.java
```

`untracked` significa que el archivo existe dentro del proyecto, pero **Git todavía no lo está siguiendo**.

Si posteriormente modificas un archivo que ya estaba controlado por Git, `git status` puede mostrar:

```
modified: Main.java
```

Esto significa que el archivo ha cambiado desde el último estado registrado.

También puede mostrar archivos que ya has preparado para guardar, algo que veremos cuando estudiemos `git add`.

`git status` **no modifica ningún archivo ni guarda ningún cambio**. Solo consulta el estado del repositorio.