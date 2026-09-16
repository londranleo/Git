# Seguimiento de ramas remotas

El **seguimiento de ramas remotas** permite que una rama local sepa **con qué rama del repositorio remoto está relacionada**.

Por ejemplo:

```
Local                         Remoto

main  ───────────────────→  origin/prueba
```

Aquí la rama local `main` está siguiendo a `origin/main`.

Esto permite ejecutar simplemente:

```bash
git pull
```

en lugar de tener que indicar cada vez:

```bash
git pull origin prueba
```

Lo mismo ocurre con `git push`:

```bash
git push
```

Git ya sabe que debe enviar los commits de `prueba` hacia `origin/prueba`.

La relación de seguimiento normalmente se establece al hacer:

```bash
git push -u origin prueba
```

La opción `-u` establece el **upstream**, es decir, la rama remota que seguirá tu rama local.

También puedes comprobar las relaciones entre ramas con:

```bash
git branch -vv
```

Podrías ver:

```
* prueba  a82f31c [origin/main] Añadir documentación
  master  7bc921c
```

En este ejemplo, `prueba` está vinculada a `origin/prueba`, mientras que `master` no tiene una rama remota asociada.