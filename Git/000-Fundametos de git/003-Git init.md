# Git init

`git init` es el comando que **inicializa un repositorio Git dentro de una carpeta**.

Supongamos que tienes un proyecto:

```
MiProyecto/
├── src/
└── pom.xml
```

Todavía es simplemente una carpeta. Si ejecutas dentro de ella:

```
git init
```

Git crea una carpeta oculta:

```
MiProyecto/
├── .git/
├── src/
└── pom.xml
```

`.git` contiene la información interna que Git necesita para gestionar ese repositorio: historial, referencias, configuración, objetos de Git, etc.

A partir de ese momento, los comandos de Git que ejecutes dentro de `MiProyecto` trabajarán sobre ese repositorio.

Por ejemplo:

```
cd MiProyecto
git init
```

No necesitas ejecutar `git init` cada vez que abras el proyecto. **La inicialización se hace para crear el repositorio; después simplemente trabajas con él.**