# Git tag 

`git tag` sirve para **poner un nombre a un commit concreto** del historial.

A diferencia de una rama, un tag normalmente se utiliza para **marcar un punto importante y estable del proyecto**, como una versión.

Por ejemplo, cuando terminas una versión de tu aplicación:

```
git tag v1.0.0
```

El tag queda asociado al commit en el que te encuentras:

```
A → B → C
         ↑
       v1.0.0
```

El commit sigue teniendo su hash, pero ahora también puedes identificarlo fácilmente mediante `v1.0.0`.

Puedes ver los tags existentes con:

```
git tag
```

Y consultar qué commit corresponde a uno:

```
git show v1.0.0
```

La diferencia importante con una rama es que **una rama está pensada para avanzar con nuevos commits**, mientras que un tag se utiliza normalmente para **marcar un punto concreto del historial**, como una versión publicada.

Los tags serán especialmente útiles en el siguiente punto, **Releases**, donde veremos cómo se utilizan para identificar versiones de un proyecto.