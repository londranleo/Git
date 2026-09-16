# Git clone

`git clone` sirve para **crear una copia local de un repositorio remoto**.

Es decir, si tienes un proyecto en GitHub y quieres trabajar con él desde tu ordenador, puedes clonarlo:

```
git clone https://github.com/usuario/MiProyecto.git
```

Git descargará el repositorio y creará una carpeta:

```
MiProyecto/
├── src/
├── pom.xml
└── .git/
```

Lo importante es que `clone` no descarga únicamente los archivos del proyecto. También obtiene la información necesaria del repositorio Git, incluyendo su historial y las referencias necesarias para trabajar con él.

Por eso, después de clonar un repositorio ya puedes ejecutar:

```
git log
```

y consultar su historial.

Además, Git configura automáticamente una conexión con el repositorio remoto que has clonado, normalmente utilizando el nombre `origin`.

La diferencia con `git init` es fundamental:

```
git init
→ tienes un proyecto local
→ conviertes esa carpeta en un repositorio Git

git clone
→ ya existe un repositorio remoto
→ creas una copia local de ese repositorio
```

Por ejemplo, si encuentras un proyecto en GitHub que quieres modificar, normalmente utilizarías `git clone` en lugar de crear un repositorio vacío con `git init`.