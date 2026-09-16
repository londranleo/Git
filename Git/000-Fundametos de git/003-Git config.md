# Git config

`git config` sirve para **configurar el comportamiento de Git**.

Antes de empezar a trabajar normalmente debes decirle a Git **quién eres**, porque esa información aparecerá asociada a los commits que hagas.

Git permite establecer esta configuración en **tres niveles**:

```Bash
--system
--global
--local
```

### `--system`

```bash
git config --system user.name "Nombre"
```

Establece una configuración de Git que se aplica **a todos los usuarios y a todos los repositorios del ordenador**. Se utiliza para configurar Git a nivel del sistema y normalmente requiere permisos de administrador.

### `--global`

```Bash
git config --global user.name "Leo"
git config --global user.email "leo@gmail.com"
```

Establece la configuración **predeterminada para el usuario actual del sistema**. Todos los repositorios de ese usuario utilizarán estos datos, salvo que un repositorio tenga una configuración `--local` diferente.

### `--local`

```bash
git config --local user.name "Leo-Portatil"
git config --local user.email "trabajo@gmail.com"
```

Establece una configuración que **solo se aplica al repositorio actual**. Se guarda dentro de `.git/config`.

Puedes tener las tres configuraciones al mismo tiempo. Cuando una misma opción está configurada en varios niveles, Git utiliza la de mayor prioridad:

```
--system
    ↓
--global
    ↓
--local
```

Por ejemplo, si tienes:

```
Global:
user.name = Leo

Local:
user.name = Leo-Portatil
```

dentro de ese repositorio Git utilizará:

```
Leo-Portatil
```

porque la configuración local tiene prioridad sobre la global.

Para consultar la configuración puedes utilizar:

```
git config --system --list
git config --global --list
git config --local --list
```

Y para consultar un valor concreto:

```
git config --global user.name
git config --local user.name
```

En la práctica, **`--global` suele utilizarse para tu configuración habitual y `--local` para excepciones en proyectos concretos**.

>Guardar las credenciales cuando hacemos `git push`. 

```
git config --global credential.helper=store
```

Ahora cuando ejecutemos `git push` nos pedira autentidicacion, `Username` tu id de tu github o uno inventado, `Password` aqui hay tener un **Personal access tokens**.

```
Username for 'https://github.com': 
Password for 'https://londranleo@github.com':
```


