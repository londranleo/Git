# Eliminar ramas

Una rama puede eliminarse cuando **ya no necesitas esa línea de desarrollo**, por ejemplo, después de integrar sus cambios en `main`.

Eliminar una rama **no significa eliminar automáticamente los commits que contiene**. Lo que se elimina es la **referencia que apunta a esos commits**.

Para eliminar una rama local:

```
git branch -d desarrollo
```

La opción `-d` es una eliminación segura: Git comprueba si la rama ya ha sido integrada antes de eliminarla.

Si intentas eliminar una rama que contiene cambios que todavía no han sido integrados, Git normalmente impedirá la operación para evitar que pierdas trabajo accidentalmente.

También existe:

```
git branch -D desarrollo
```

`-D` fuerza la eliminación aunque Git detecte que sus cambios no han sido integrados.

Por eso `-D` debe utilizarse con más cuidado.

En esta etapa estamos hablando de **ramas locales**. Más adelante veremos cómo eliminar una rama que existe en el repositorio remoto.