# Pull Requests

Una **Pull Request (PR)** es una propuesta para **integrar los cambios de una rama en otra**, normalmente en GitHub.

La idea es que no tengas que incorporar directamente tus cambios a la rama principal. Primero trabajas en una rama independiente y después propones que esos cambios sean revisados.

Por ejemplo:

```
main
  │
  └── desarrollo
        ├── cambio 1
        └── cambio 2
```

Cuando terminas, creas una Pull Request para solicitar:

```
desarrollo → main
```

En la Pull Request se pueden revisar los cambios antes de incorporarlos. Otras personas pueden:

- revisar el código;
- comentar cambios concretos;
- solicitar modificaciones;
- aprobar la propuesta.

Una vez aprobada, los cambios pueden integrarse en `main`.

La Pull Request **no es un comando de Git**. Es una función proporcionada por plataformas como GitHub para facilitar la colaboración sobre repositorios Git.

El flujo típico es:

```
Crear rama
↓
Trabajar y hacer commits
↓
Subir la rama al remoto
↓
Crear Pull Request
↓
Revisar cambios
↓
Integrar en main
```