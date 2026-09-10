# Catch

`catch` es el bloque que permite **capturar y gestionar una excepción** que se produzca dentro de un bloque `try`.

Mientras que `try` define **qué código puede producir una excepción**, `catch` define **qué hacer cuando esa excepción ocurre**.

La estructura es:

```java
try {
    // código que puede producir una excepción
} catch (Exception e) {
    // código para gestionar la excepción
}
```

Cuando Java encuentra una excepción dentro del `try`, **detiene la ejecución normal de ese bloque** y busca un `catch` cuyo tipo sea compatible con la excepción producida.

Conceptualmente:

```
try
 │
 ├── no hay excepción → continúa normalmente
 │
 └── hay excepción
          ↓
       catch
          ↓
   gestiona el problema
```

El tipo indicado en `catch` determina **qué excepciones puede capturar**.

```java
try {
    int numero = Integer.parseInt("abc");
} catch (NumberFormatException e) {
    System.out.println("El valor no es un número válido");
}
```

En este caso, `catch` captura específicamente `NumberFormatException`.

La variable `e` contiene el **objeto de la excepción**, que proporciona información sobre lo ocurrido. A través de él podemos consultar información como el mensaje asociado a la excepción.

También podemos tener **varios `catch`** después de un mismo `try`, permitiendo tratar diferentes tipos de excepciones de manera diferente.

Es importante que los `catch` estén ordenados correctamente: un `catch` más general no debe aparecer antes de uno más específico que herede de él.

>`catch` es el mecanismo que permite **capturar una excepción producida dentro de `try` y ejecutar un tratamiento específico para ella**.