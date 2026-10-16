## `else if`

`else if` permite **comprobar otra condición cuando la condición anterior de un `if` es falsa**.
Se utiliza cuando tenemos **más de dos posibilidades** y necesitamos comprobarlas en orden.

Su estructura es:

```java
if (condición1) {
    // código
} else if (condición2) {
    // código
} else {
    // código si ninguna condición se cumple
}
```

Java comprueba las condiciones **de arriba hacia abajo**:

1. Comprueba el `if`.
2. Si es `true`, ejecuta su bloque y termina la estructura.
3. Si es `false`, comprueba el siguiente `else if`.
4. Continúa así hasta encontrar una condición verdadera.
5. Si ninguna es verdadera, ejecuta el `else`, si existe.

Por ejemplo:

```java
if (nota >= 9) {
    System.out.println("Excelente");
} else if (nota >= 5) {
    System.out.println("Aprobado");
} else {
    System.out.println("Suspenso");
}
```

Aunque varias condiciones podrían ser verdaderas al mismo tiempo, **solo se ejecuta el primer bloque cuya condición resulte verdadera**.

El `else` final es opcional. Podemos utilizar varios `else if`, pero solamente puede existir **un `else` y siempre debe estar al final**.

> `else if` permite crear varias alternativas. Java las comprueba en orden y ejecuta únicamente el primer bloque cuya condición sea verdadera.