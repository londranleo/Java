## Operadores relacionales

Los **operadores relacionales** se utilizan para **comparar dos valores** y determinar qué relación existe entre ellos.

El resultado de una comparación siempre es un valor de tipo **`boolean`**, es decir, `true` o `false`.

Los principales operadores son:

|Operador|Significado|
|---|---|
|`>`|Mayor que|
|`<`|Menor que|
|`>=`|Mayor o igual que|
|`<=`|Menor o igual que|

Por ejemplo:

```java
int edad = 22;

edad >= 18; // true
```

La expresión no modifica `edad`; simplemente **compara su valor** y produce un resultado booleano.

Los operadores relacionales se utilizan principalmente para construir **condiciones**, por lo que aparecen constantemente en estructuras como `if`, `while` y `for`.

También pueden utilizarse con expresiones, no únicamente con variables:

```java
10 + 5 > 12; // true
```

Java primero evalúa la expresión y posteriormente realiza la comparación.

Es importante diferenciar los operadores relacionales de los operadores de **igualdad**. Los relacionales comprueban relaciones como mayor o menor, mientras que `==` y `!=` comprueban si dos valores son iguales o diferentes.