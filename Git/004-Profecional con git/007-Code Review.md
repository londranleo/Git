# Code Review

El **Code Review** es el proceso de **revisar el código antes de incorporarlo al proyecto**, normalmente antes de aceptar una Pull Request.

Su objetivo no es solamente buscar errores. También sirve para comprobar que el código:

- funciona correctamente;
- es comprensible y mantenible;
- sigue las reglas y convenciones del proyecto;
- no introduce problemas innecesarios.

Por ejemplo, una persona crea una Pull Request con una nueva funcionalidad. Otro desarrollador revisa los cambios y puede dejar comentarios como:

> Esta parte podría simplificarse.

o:

> Aquí falta controlar este caso.

El autor puede modificar el código y actualizar la misma Pull Request. La revisión continúa hasta que los cambios cumplen los criterios del proyecto.

Por tanto:

```
Pull Request
→ propuesta para integrar cambios

Code Review
→ revisión de esos cambios antes de integrarlos
```

El Code Review es especialmente importante en equipos porque **varias personas revisan el código antes de que llegue a una rama importante como `main`**.