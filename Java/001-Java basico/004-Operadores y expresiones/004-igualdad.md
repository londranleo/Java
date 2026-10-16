## Operadores de igualdad

Los **operadores de igualdad** se utilizan para determinar si dos valores son **iguales o diferentes**. Al igual que los operadores relacionales, el resultado de la comparación siempre es un valor `boolean`: `true` o `false`.

Java dispone de dos operadores de igualdad:

| Operador | Significado  | Valores                                       |
| -------- | ------------ | ------------------------------------------ |
| `==`     | Igual a                                                      |
| `!=`     | Difer true si son distinto, false si son iguales on  se  o,  |

### `==`

Comprueba si los dos operandos son iguales.

```java
int edad = 22;

edad == 22; // true
```

En el caso de los **tipos primitivos**, `==` compara directamente los valores.

Sin embargo, cuando se utiliza con **objetos**, `==` compara las **referencias**, es decir, comprueba si ambas variables hacen referencia al mismo objeto. No comprueba si los objetos contienen la misma información.

Por eso, para comparar el contenido de objetos como `String`, normalmente se utiliza `equals()`.

### `!=`

Comprueba si los dos operandos son diferentes.

```java
int edad = 22;

edad != 18; // true
```

Con tipos primitivos, compara sus valores. Con objetos, al igual que `==`, compara las referencias.

Los operadores `==` y `!=` tienen una relación directa: uno comprueba igualdad y el otro desigualdad. Ambos producen siempre un resultado booleano.

Estas comparaciones son especialmente importantes al construir condiciones, ya que permiten que el programa determine qué camino debe seguir dependiendo de si determinados valores coinciden o son diferentes.