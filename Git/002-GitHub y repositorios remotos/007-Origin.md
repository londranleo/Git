# Origin 

`origin` es el **nombre que Git asigna normalmente al repositorio remoto principal** cuando lo conectas mediante `git remote add` o cuando clonas un repositorio.

Por ejemplo:

```
git remote add origin https://github.com/usuario/proyecto.git
```

Aquí `origin` es simplemente un **nombre para identificar ese remoto**.

Puedes comprobarlo con:

```bash
git remote -v
```

Y ver algo como:

```bash
origin  https://github.com/usuario/proyecto.git (fetch)
origin  https://github.com/usuario/proyecto.git (push)
```

Esto permite utilizar comandos como:

```bash
git fetch origin
git pull origin main
git push origin main
```

En estos comandos:

```
origin → ¿a qué repositorio remoto?
main   → ¿qué rama?
```

`origin` **no es el repositorio remoto en sí**, sino el nombre local que Git utiliza para referirse a esa conexión.

También puedes tener varios remotos:

```
origin → repositorio principal
upstream → otro repositorio
```

y utilizarlos por separado.