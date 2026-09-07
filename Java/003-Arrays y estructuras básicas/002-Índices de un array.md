## Índices de un array

Cada elemento de un array tiene una **posición llamada índice**. El índice permite identificar exactamente qué elemento queremos consultar o modificar.

En Java, los índices de un array **siempre comienzan en `0`**.

Por ejemplo:

```java
int[] numeros = {10, 20, 30, 40};
```

Sus posiciones serían:

```java
Índice:   0    1    2    3
Valor:   10   20   30   40
```

Por tanto:

```java
numeros[0]  // 10
numeros[2]  // 30
```

El **último índice** siempre es igual al tamaño del array menos uno:

```java
último índice = longitud - 1
```

Podemos conocer el número de elementos mediante la propiedad `length`:

```java
numeros.length
```

En el ejemplo anterior, `length` vale `4`, por lo que el último índice es `3`.

Los índices también permiten **modificar elementos**:

```java
numeros[1] = 50;
```

Ahora el segundo elemento pasa de `20` a `50`.

Es importante no confundir **índice** con **posición humana**. Si hablamos de "primer elemento", normalmente pensamos en la posición 1, pero Java lo identifica mediante el índice `0`.

Si intentamos utilizar un índice negativo o uno igual o superior a `length`, el índice no existe y Java lanza una `ArrayIndexOutOfBoundsException`.

> el índice identifica la posición de cada elemento dentro del array. Comienza en `0` y termina en `length - 1`.