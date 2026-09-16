# Git push

`git push` sirve para **enviar los commits de tu repositorio local al repositorio remoto**.

Por ejemplo, tienes:

```
LOCAL                         REMOTO
A → B → C                     A → B
```

Has creado el commit `C` en tu ordenador, pero todavía no está en GitHub.

Cuando ejecutas:

```
git push
```

Git envía el commit al repositorio remoto:

```
LOCAL                         REMOTO
A → B → C                     A → B → C
```

Es importante entender que `git push` **no envía simplemente los archivos modificados**. Lo que sincroniza principalmente son los commits y las referencias correspondientes.

Antes de hacer `push`, normalmente el proceso es:

```
Modificar archivos
      ↓
git add
      ↓
git commit
      ↓
git push
      ↓
Repositorio remoto
```

Por ejemplo:

```
git add .
git commit -m "Añadir sistema de login"
git push
```

Si es la primera vez que estás subiendo una rama y Git todavía no sabe qué rama remota debe seguir, puedes establecerla:

```
git push -u origin main
```

La opción `-u` establece una relación de seguimiento entre tu rama local y la rama remota. Después de configurarla, normalmente podrás utilizar simplemente:

```
git push
```

`git push` **no descarga cambios del remoto**. Su función es llevar tus cambios confirmados desde el repositorio local hacia el remoto.