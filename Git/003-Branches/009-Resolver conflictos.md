# Resolver conflictos

Resolver un conflicto significa **decidir qué cambios deben quedar cuando Git no puede hacer el `merge` automáticamente**.

Cuando aparece un conflicto, el proceso es:

1. Git marca el archivo conflictivo.
2. Tú revisas las dos versiones.
3. Decides qué código conservar, modificar o combinar.
4. Eliminas las marcas que Git añadió.
5. Guardas el archivo.
6. Indicas a Git que el conflicto está resuelto con:

```
git add <archivo>
```

7. Finalizas el `merge` con:

```
git commit
```

Por ejemplo, si Git encuentra:

```
<<<<<<< HEAD
Hola
=======
Buenas
>>>>>>> desarrollo
```

tú decides qué debe quedar. Podría quedar:

```
Hola
```

o:

```
Buenas
```

o incluso una combinación diferente.

Después:

```
git add archivo.txt
git commit
```

El `git add` en este contexto **no está creando un commit**. Le está indicando a Git:

> "He resuelto este conflicto y esta es la versión que quiero conservar."

Una vez resueltos todos los archivos conflictivos, el `merge` puede finalizar.

Si durante el conflicto decides que **no quieres continuar con el merge**, puedes cancelarlo con:

```
git merge --abort
```

Esto intenta devolver el repositorio al estado que tenía antes de comenzar el `merge`.