# Git pull

`git pull` sirve para **traer los cambios del repositorio remoto a tu rama local e integrarlos en ella**.

Por ejemplo:

```
GitHub
A → B → C

Tu PC
A → B
```

Si ejecutas:

```bash
git pull
```

Git obtiene `C` del remoto y lo integra en tu rama local:

```
Tu PC
A → B → C
```

Conceptualmente, `git pull` combina dos operaciones:

```
git fetch
     ↓
descarga los cambios
     ↓
git merge
     ↓
integra los cambios en tu rama
```

Por eso la diferencia principal es:

```
git fetch
→ descarga información
→ no modifica tu rama actual

git pull
→ descarga información
→ integra esos cambios en tu rama actual
```

Por ejemplo, si estás trabajando en la rama `main`:

```bash
git switch prueba
git pull
```

Git buscará los nuevos cambios de la rama remota que `main` esté siguiendo y los integrará en tu rama local.