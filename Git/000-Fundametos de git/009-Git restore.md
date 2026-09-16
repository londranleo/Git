# Git restore

`git restore` sirve para **descartar cambios que has hecho en tus archivos y devolverlos a un estado anterior**.

Por ejemplo, tienes un archivo que Git ya conoce:

```
Main.java
```

Lo modificas y decides que **no quieres conservar esos cambios**.

Puedes ejecutar:

```
git restore Main.java
```

Git reemplazará el contenido actual de `Main.java` por el contenido que tenía en el estado registrado que estás usando como referencia.

Esto es útil cuando haces cambios, pruebas cosas y finalmente decides:

> "No quiero ninguno de estos cambios."

También puede utilizarse para sacar un archivo de la **Staging Area**:

```
git restore --staged Main.java
```

En este caso **no elimina tus modificaciones**. Simplemente quita `Main.java` de la Staging Area y vuelve a dejar esos cambios como modificaciones normales.

Por tanto:

```
git restore archivo
→ descarta los cambios del archivo

git restore --staged archivo
→ saca el archivo de staging, pero conserva sus cambios
```

La diferencia es importante porque el primer comando puede **hacerte perder los cambios que hayas realizado**.