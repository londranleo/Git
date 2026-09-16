# Repositorio
Un **repositorio** es el espacio donde Git guarda y administra la información relacionada con un proyecto.

Cuando hablamos de un repositorio Git, normalmente nos referimos a una carpeta de proyecto que contiene la carpeta oculta `.git`.

Por ejemplo:

```
MiAplicacion/
├── src/
├── pom.xml
└── .git/
```

La carpeta `.git` es la que permite a Git conocer el historial del proyecto, sus commits, ramas y demás información necesaria para gestionar las versiones.

Por eso, una carpeta normal **no es todavía un repositorio Git**. Se convierte en uno cuando inicializas Git dentro de ella con:

```
git init
```

A partir de ahí:

```
Carpeta normal
      ↓
   git init
      ↓
Repositorio Git
```