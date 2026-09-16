# Git add

`git add` sirve para **preparar cambios para el próximo commit**.

Aquí aparece un concepto importante de Git: la **Staging Area**.

Git no pasa directamente de tus archivos a un commit. Existe una zona intermedia donde seleccionas exactamente qué cambios quieres incluir.

El proceso es:

```
Tus archivos
     ↓
git add
     ↓
Staging Area
     ↓
git commit
     ↓
Historial de Git
```

Por ejemplo, tienes:

```
MiProyecto/
├── Main.java
├── Usuario.java
└── Conexion.java
```

Has modificado `Main.java` y `Usuario.java`, pero todavía no quieres incluir `Conexion.java`.

Puedes hacer:

```
git add Main.java Usuario.java
```

Ahora esos dos archivos están en la **Staging Area** y serán incluidos cuando hagas el siguiente commit.

También puedes preparar todos los cambios:

```
git add .
```

El punto `.` significa **la carpeta actual y su contenido**.

Importante: `git add` **no crea una versión ni guarda el cambio definitivamente**. Solo selecciona/prepara los cambios que posteriormente serán registrados mediante `git commit`.