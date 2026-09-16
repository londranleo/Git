# Conflictos de merge

Un **conflicto de merge** ocurre cuando Git intenta unir dos ramas y **no puede decidir automáticamente qué cambio debe conservar**.

Normalmente Git puede combinar los cambios por sí mismo. El problema aparece cuando **las dos ramas han modificado la misma parte de un archivo de manera incompatible**.

Por ejemplo, `main` tiene:

```
mensaje = "Hola"
```

y `desarrollo` ha cambiado esa misma línea a:

```
mensaje = "Buenas"
```

Si ambas ramas modificaron esa misma línea de forma diferente, Git no puede asumir cuál de las dos versiones quieres.

Cuando haces el `merge`, Git marca el archivo como **conflictivo** y detiene la integración.

Dentro del archivo encontrarás marcas similares a:

```
<<<<<<< HEAD
mensaje = "Hola"
=======
mensaje = "Buenas"
>>>>>>> desarrollo
```

Estas marcas indican:

```
<<<<<<< HEAD
→ versión de la rama en la que estás

=======
→ separación entre ambas versiones

>>>>>>> desarrollo
→ versión de la rama que estás integrando
```

En ese momento **Git no ha elegido ninguna versión**. Tú debes decidir qué código debe quedar y eliminar las marcas del conflicto.

El conflicto no significa que Git esté roto ni que hayas perdido los cambios. Significa que **Git necesita que tú decidas cómo combinar esas dos modificaciones**.

El siguiente punto será **resolver conflictos**, donde veremos exactamente qué hacer después de que aparezca uno.