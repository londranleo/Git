# Buenas prácticas de commits

Las buenas prácticas de commits consisten en **organizar el historial de Git para que sea claro, útil y fácil de mantener**.

Un commit debería representar **un cambio concreto y coherente**. La idea es que, al mirar el historial, puedas entender qué se hizo sin tener que revisar todo el código.

Por ejemplo, es mejor separar:

```
Añadir sistema de login
Corregir validación de usuario
Actualizar documentación
```

que hacer un único commit:

```
Cambios
```

También conviene evitar commits que mezclen cambios que no tienen relación entre sí. Si estás corrigiendo un error de login, no deberías aprovechar el mismo commit para modificar veinte cosas diferentes del proyecto.

El historial debería permitir entender **cómo ha evolucionado el proyecto** y facilitar tareas posteriores como revisar cambios, encontrar errores o revertir una modificación concreta.

Una buena práctica general es:

> **Un commit debe contener un cambio lógico y tener un mensaje que explique claramente qué cambio se realizó.**