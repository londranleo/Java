## Copia de arrays

Copiar un array significa **crear otro array a partir de los elementos de uno existente**.

Es importante entender que asignar un array a otra variable **no crea una copia**:

```java
int[] a = {10, 20, 30};
int[] b = a;
```

En este caso, `a` y `b` hacen referencia al **mismo array**. Si modificamos `b`, también veremos el cambio al acceder mediante `a`.

Para crear realmente otro array podemos utilizar diferentes métodos.

### `Arrays.copyOf()`

Permite crear una nueva copia del array indicando el tamaño que tendrá:

```java
int[] copia = Arrays.copyOf(a, a.length);
```

El resultado es un **array independiente** del original.

También podemos indicar un tamaño diferente. Si el nuevo tamaño es mayor, las posiciones adicionales se rellenan con el valor predeterminado del tipo.

### `Arrays.copyOfRange()`

Permite copiar **una parte concreta** de un array:

```
int[] copia = Arrays.copyOfRange(a, 1, 3);
```

El índice inicial se incluye, pero el índice final **no se incluye**.

Por tanto, se copian los elementos de los índices `1` y `2`.

### Copia mediante `clone()`

Los arrays también proporcionan `clone()`, que permite crear una copia del array:

```
int[] copia = a.clone();
```

Al igual que `Arrays.copyOf()`, produce un nuevo array.

### Copia superficial

Cuando hablamos de arrays de **tipos primitivos**, copiar el array significa copiar directamente sus valores.

Sin embargo, cuando un array contiene **objetos**, la situación es diferente. La copia crea un nuevo array, pero sus elementos siguen siendo referencias a los mismos objetos.

Esto se conoce como **copia superficial (shallow copy)**.

Por eso, copiar un array no significa necesariamente copiar todos los objetos que contiene.

> asignar un array a otra variable no lo copia; ambas variables apuntan al mismo array. Para crear un nuevo array podemos utilizar `Arrays.copyOf()`, `Arrays.copyOfRange()` o `clone()`. En arrays de objetos, estas copias son superficiales.