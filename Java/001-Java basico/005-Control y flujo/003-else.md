## `else`

`else` permite indicar **qué código ejecutar cuando la condición de un `if` no se cumple**.

Mientras que `if` se ejecuta cuando la condición es `true`, `else` se ejecuta cuando esa condición es `false`.

Su estructura es:

```java
if (condición) {
    // si la condición es true
} else {
    // si la condición es false
}
```

Por ejemplo:

```java
if (edad >= 18) {
    System.out.println("Mayor de edad");
} else {
    System.out.println("Menor de edad");
}
```

Si `edad` es `20`, se ejecuta el bloque del `if`. Si `edad` es `15`, se ejecuta el bloque del `else`.

`else` **siempre está asociado a un `if`** y no necesita una condición propia, ya que representa automáticamente el caso contrario de la condición del `if`.

También puede combinarse con `else if` cuando existen **más de dos posibilidades**, que veremos a continuación.

>`else` permite definir qué ocurre cuando la condición del `if` es falsa. Así podemos establecer un comportamiento tanto para el caso verdadero como para el caso contrario.