# Git remote

`git remote` sirve para **gestionar la conexión entre tu repositorio local y un repositorio remoto**.

Hasta ahora tu proyecto puede existir únicamente en tu ordenador:

```
MiProyecto/
└── .git/
```

Si quieres conectarlo con un repositorio que ya existe en GitHub, tienes que indicarle a Git **dónde está ese repositorio remoto**.

Para añadirlo:

```
git remote add origin https://github.com/usuario/MiProyecto.git
```

Para cambiar la url:

```
git remote set-url origin "direccion repositorio"
```

Aquí:

- `remote` → trabajas con repositorios remotos.
- `add` → añades una nueva conexión.
- `origin` → nombre que le das a esa conexión.
- La URL → dirección del repositorio remoto.

Después puedes comprobar qué repositorios remotos tienes configurados:

```
git remote -v
```

Podrías obtener:

```
origin  https://github.com/usuario/MiProyecto.git (fetch)
origin  https://github.com/usuario/MiProyecto.git (push)
```

`origin` es simplemente el **nombre que identifica al remoto**. Es el nombre convencional que Git utiliza normalmente para el repositorio remoto principal, pero técnicamente podrías llamarlo de otra forma.

Todavía no estás enviando ningún archivo a GitHub. `git remote add` **solo establece la conexión**.