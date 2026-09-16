# `.gitignore`

`.gitignore` es un archivo que le indica a Git **qué archivos o carpetas debe ignorar y no tener en cuenta para el control de versiones**.

Esto es útil porque en un proyecto existen archivos que **no deberían formar parte del repositorio**, aunque estén dentro de la carpeta del proyecto.

Por ejemplo, en un proyecto Java puedes tener:

```
proyecto/
├── src/
├── pom.xml
├── target/
└── .idea/
```

`target/` contiene archivos generados automáticamente al compilar, y `.idea/` puede contener configuraciones específicas de tu IDE. Normalmente no quieres subirlos al repositorio.

Puedes crear:

```
.gitignore
```

y escribir:

```
target/
.idea/
*.class
```

A partir de ahí, Git ignorará esos archivos cuando compruebe qué cambios existen.

Es importante entender que **`.gitignore` no borra archivos de tu ordenador**. Simplemente le dice a Git que **no los incluya como archivos pendientes de seguimiento**.

También hay una diferencia importante: si un archivo **ya está siendo seguido por Git**, añadirlo posteriormente a `.gitignore` no hace que Git deje de seguirlo automáticamente. En ese caso hay que eliminarlo del seguimiento mediante otros comandos.