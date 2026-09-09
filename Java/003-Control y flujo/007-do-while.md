## `do-while`

`do-while` es una estructura de control que permite **repetir un bloque de código mientras se cumpla una condición**.

La diferencia principal con `while` es **cuándo se comprueba la condición**.

Su estructura es:

```java
do {
    // código que se repite
} while (condición);
```

En `do-while`, Java **ejecuta primero el bloque y después comprueba la condición**.

- Se ejecuta el bloque.
- Se comprueba la condición.
- Si es `true`, vuelve a ejecutar el bloque.
- Si es `false`, termina el bucle.

Por esta razón, un `do-while` **siempre ejecuta su bloque al menos una vez**, incluso aunque la condición sea falsa desde el principio.

```java
int numero = 10;

do {
    System.out.println(numero);
} while (numero < 5);
```

Aunque `numero < 5` es `false`, el mensaje se muestra una vez porque el bloque se ejecuta antes de comprobar la condición.

Esto hace que `do-while` sea útil cuando **necesitamos ejecutar algo al menos una vez** y después decidir si debe repetirse.

Una diferencia importante es:

```java
while       → comprueba → ejecuta
do-while    → ejecuta → comprueba
```

>`do-while` repite un bloque mientras una condición sea verdadera, pero a diferencia de `while`, **el bloque se ejecuta siempre al menos una vez**.