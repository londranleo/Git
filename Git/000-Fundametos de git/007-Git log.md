# Git log

`git log` sirve para **consultar el historial de commits de un repositorio**.

Después de haber creado varios commits:

```
git commit -m "Crear proyecto"
git commit -m "Añadir usuarios"
git commit -m "Conectar MySQL"
```

puedes ejecutar:

```
git log
```

Git mostrará los commits realizados, normalmente incluyendo información como:

```
commit a82f31...
Author: Leo
Date:   ...

    Conectar MySQL

commit 7bc921...
Author: Leo
Date:   ...

    Añadir usuarios

commit 31d4aa...
Author: Leo
Date:   ...

    Crear proyecto
```

Cada commit tiene un **identificador único**, normalmente representado mediante un hash. Ese identificador permite referirse exactamente a una versión concreta del proyecto.

El historial aparece normalmente desde el **commit más reciente hacia el más antiguo**.

También puedes utilizar:

```
git log --oneline
```

para obtener una versión más compacta:

```
a82f31 Conectar MySQL
7bc921 Añadir usuarios
31d4aa Crear proyecto
```

`git log` solamente consulta el historial; no modifica el proyecto.