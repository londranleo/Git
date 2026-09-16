# Crear ramas

Aunque ya hemos utilizado `git branch` y `git switch`, ahora vamos a centrarnos en **cómo se crea una rama y desde dónde se crea**.

Cuando creas una rama, esta comienza apuntando al **commit en el que te encuentras actualmente**.

Por ejemplo:

```
A → B → C
         ↑
        main
        ↑
       HEAD
```

Si ejecutas:

```
git switch -c desarrollo
```

Git crea `desarrollo` desde `C` y te cambia a ella:

```
A → B → C
         ↑
        main
         \
          desarrollo
              ↑
             HEAD
```

A partir de aquí, si haces un commit:

```
git commit -m "Añadir funcionalidad"
```

obtienes:

```
A → B → C
         ↑
        main
         \
          D
           ↑
       desarrollo
           ↑
          HEAD
```

`main` sigue apuntando a `C`, mientras que `desarrollo` avanza hacia `D`.

Esto es lo importante al crear ramas: **la rama nueva parte del commit actual**, por lo que el lugar desde el que la creas determina qué historial tendrá inicialmente.

También puedes crear una rama sin cambiarte a ella:

```
git branch desarrollo
```

y posteriormente cambiarte:

```
git switch desarrollo
```

La forma más habitual cuando quieres empezar inmediatamente a trabajar en una nueva rama es:

```
git switch -c desarrollo
```