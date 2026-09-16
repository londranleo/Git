# Releases

Una **Release** es una versión concreta y preparada de un proyecto que se publica para que otras personas puedan utilizarla.

Una Release normalmente está asociada a un **tag**, que identifica exactamente qué commit corresponde a esa versión.

Por ejemplo:

```
A → B → C → D
         ↑
       v1.0.0
```

Si creas una Release `v1.0.0`, estás diciendo:

> Esta es la versión 1.0.0 del proyecto y corresponde exactamente a este punto del historial.

Una Release puede incluir información adicional sobre esa versión, como:

- qué funcionalidades se añadieron;
- qué errores se corrigieron;
- cambios importantes;
- archivos que los usuarios pueden descargar.

La diferencia entre ambos conceptos es:

```
Tag
→ marca un commit concreto.

Release
→ presenta ese punto del proyecto como una versión publicada.
```

Por ejemplo, puedes tener:

```
v1.0.0 → primera versión estable
v1.1.0 → nueva funcionalidad
v1.1.1 → corrección de errores
```

En Git, el tag identifica el punto exacto del código; en GitHub, la Release utiliza ese tag para representar y documentar una versión del proyecto.