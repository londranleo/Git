# Convenciones de mensajes

Las **convenciones de mensajes** son reglas para escribir los mensajes de los commits de una forma **consistente y fácil de entender**.

El mensaje debe indicar **qué cambio se realizó**, de forma breve y específica.

Por ejemplo:

```
git commit -m "Añadir validación de usuario"
```

Es mejor que:

```
git commit -m "Cambios"
```

Una convención bastante utilizada es **Conventional Commits**, que clasifica el tipo de cambio:

```
feat: añadir sistema de login
fix: corregir validación del usuario
docs: actualizar documentación
refactor: reorganizar ClienteService
test: añadir pruebas de Cliente
```

Los tipos indican la naturaleza del cambio:

- `feat` → nueva funcionalidad.
- `fix` → corrección de un error.
- `docs` → documentación.
- `refactor` → reorganización del código sin cambiar su comportamiento.
- `test` → pruebas.
- `chore` → tareas de mantenimiento.

No es obligatorio utilizar esta convención en Git. **Es una forma de estandarizar los mensajes para que todo el equipo escriba los commits de manera uniforme.**