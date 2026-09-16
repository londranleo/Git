# Git commit --ammed

`git commit --amend` sirve para **modificar el último commit que has creado**, en lugar de crear uno nuevo.

Es útil cuando acabas de hacer un commit y te das cuenta de que:

- olvidaste incluir un archivo;
- hiciste un cambio pequeño que debería formar parte de ese commit;
- quieres corregir el mensaje del commit.

Por ejemplo, haces:

```
git add Main.java
git commit -m "Añadir Main"
```

Y después descubres que también querías incluir `Usuario.java`.

Puedes preparar ese archivo:

```
git add Usuario.java
```

y después:

```
git commit --amend
```

Git modificará **el último commit** para incluir también `Usuario.java`.

El historial no quedará así:

```
Commit 1 → Añadir Main
Commit 2 → Añadir Usuario
```

sino que seguirá existiendo **un solo commit**, pero ahora contendrá ambos cambios.

También puedes cambiar directamente el mensaje:

```
git commit --amend -m "Añadir clases principales"
```

###  Importante

`--amend` modifica el último commit, por lo que **cambia su identificador (hash)**.

Por eso es muy cómodo para corregir un commit que todavía estás preparando, pero debes tener cuidado si ese commit **ya lo has subido a GitHub y otras personas están trabajando sobre él**, porque estarías reescribiendo el historial.
