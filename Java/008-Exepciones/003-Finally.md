# Finally 

`finally` es un bloque que se utiliza para ejecutar código **después de un `try` y de sus posibles `catch`**.

Su característica principal es que el código de `finally` se ejecuta **tanto si ocurre una excepción como si no ocurre**.

La estructura es:

```java
try {
    // código que puede producir una excepción
} catch (Exception e) {
    // gestión de la excepción
} finally {
    // código que debe ejecutarse al finalizar
}
```

Conceptualmente:

```
              try
               │
        ┌──────┴──────┐
        ↓             ↓
   sin excepción   excepción
        │             │
        │           catch
        │             │
        └──────┬──────┘
               ↓
            finally
```

El propósito de `finally` es realizar **acciones que deben ejecutarse independientemente de que la operación haya tenido éxito o haya producido una excepción**.

Es especialmente útil para realizar tareas de **limpieza de recursos**, como cerrar archivos, conexiones o recursos que ya no necesitamos.

```
try {
    // utilizar un recurso
} catch (Exception e) {
    // gestionar el problema
} finally {
    // liberar el recurso
}
```

No debemos confundir `finally` con `catch`.

- `catch` → se ejecuta para **gestionar una excepción concreta**.
- `finally` → se utiliza para ejecutar **acciones finales**, haya ocurrido o no una excepción.

Además, `finally` puede utilizarse después de un `try` incluso sin `catch`.

```
try {
    // código
} finally {
    // código que se ejecuta al finalizar
}
```

> `finally` permite definir código que debe ejecutarse al finalizar el tratamiento del `try`, normalmente para realizar tareas de limpieza o liberar recursos, independientemente de que haya ocurrido una excepción.