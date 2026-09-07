## Arrays

Un **array** es una estructura que permite almacenar **varios valores del mismo tipo** dentro de una misma variable.

En lugar de crear una variable independiente para cada valor:

```java
int numero1 = 10;
int numero2 = 20;
int numero3 = 30;
```

podemos agruparlos en un array:

```java
int[] numeros = {10, 20, 30};
```

Todos los elementos de un array tienen **el mismo tipo**. En este caso, todos son `int`.

Una característica importante es que un array tiene un **tamaño fijo**. Cuando se crea, se establece cuántos elementos puede contener y ese tamaño no puede cambiar durante la vida del array.

También podemos crear un array indicando únicamente su tamaño:

```java
int[] numeros = new int[3];
```

Esto crea un array capaz de almacenar **3 valores `int`**. Los elementos reciben inicialmente el valor predeterminado de su tipo; para `int`, ese valor es `0`.

Cada elemento del array ocupa una posición llamada **índice**. Los índices comienzan siempre en `0`, por lo que un array de 3 elementos tiene los índices `0`, `1` y `2`.

```java
Índice:   0    1    2
Valor:   10   20   30
```

Podemos acceder a un elemento utilizando su índice:

```java
int numero = numeros[1];
```

Aquí obtenemos el segundo elemento, porque el primer elemento está en la posición `0`.

También podemos modificar un elemento:

```java
numeros[1] = 50;
```

El array pasará a contener `10, 50, 30`.

Si intentamos acceder a una posición que no existe, Java producirá una excepción `ArrayIndexOutOfBoundsException`.

>un array permite almacenar varios valores del mismo tipo bajo una misma variable. Tiene un tamaño fijo y sus elementos se identifican mediante índices que comienzan en `0`.