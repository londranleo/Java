## `while`

`while` es una estructura de control que permite **repetir un bloque de código mientras se cumpla una condición**.

A diferencia de `if`, que normalmente ejecuta un bloque como máximo una vez, `while` puede ejecutarlo **varias veces**.

Su estructura es:

```java
while (condición) {
    // código que se repite
}
```

Antes de cada repetición, Java comprueba la condición:

- Si es `true`, ejecuta el bloque.
- Al terminar, vuelve a comprobar la condición.
- Si sigue siendo `true`, vuelve a ejecutarlo.
- Cuando la condición es `false`, el bucle termina.

```java
int numero = 1;

while (numero <= 3) {
    System.out.println(numero);
    numero++;
}
```

En este caso, el bloque se ejecuta mientras `numero <= 3`.

### La condición se comprueba antes

Una característica importante de `while` es que la condición se comprueba **antes de ejecutar el bloque**.

Por eso, si la condición es `false` desde el principio, el código del `while` **no se ejecuta ninguna vez**.

Esto lo diferencia de `do-while`, donde el bloque se ejecuta al menos una vez.

### Evitar bucles infinitos

La condición debe poder llegar a ser `false`. Si nunca cambia aquello que controla la condición, el bucle puede continuar indefinidamente.

```java
while (numero <= 3) {
    // si numero nunca cambia,
    // la condición siempre será true
}
```

Por eso, normalmente dentro del bucle se modifica alguna variable que permita que finalmente termine.

>`while` repite un bloque de código mientras una condición sea verdadera. La condición se comprueba antes de cada repetición, por lo que el bloque puede ejecutarse cero, una o muchas veces.