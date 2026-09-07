## Arrays multidimensionales

Un **array multidimensional** es un array cuyos elementos son, a su vez, otros arrays. Esto permite organizar los datos en **varias dimensiones**, como filas y columnas.

El caso más común es el **array bidimensional**, que puede imaginarse como una tabla:

|      |     | Columana |     |     |
| :--: | :-: | :------: | :-: | :-: |
|      |     |    0     |  1  |  2  |
| Fila |  0  |    10    | 20  | 30  |
| Fila |  1  |    40    | 50  | 60  |

En Java se puede crear así:

```java
int[][] numeros = {
    {10, 20, 30},
    {40, 50, 60}
};
```

Aquí `numeros` contiene dos arrays internos. Por eso necesitamos **dos índices** para acceder a un elemento:

```java
numeros[0][1] // 20
```

El primer índice indica la **fila** y el segundo indica la **posición dentro de esa fila**.

Una característica importante de Java es que un array multidimensional no tiene por qué ser una tabla perfectamente rectangular. Cada array interno puede tener una longitud diferente:

```java
int[][] numeros = {
    {10, 20},
    {30, 40, 50},
    {60}
};
```

Por eso se considera realmente un **array de arrays**, y no simplemente una tabla.

Para recorrer todas sus posiciones normalmente se utilizan **bucles anidados**: un bucle recorre las filas y otro recorre los elementos de cada fila.

Los arrays pueden tener más de dos dimensiones, por ejemplo `int[][][]`, aunque su funcionamiento se basa en el mismo concepto: **cada dimensión añade otro nivel de arrays**.

>un array multidimensional es un array que contiene otros arrays. Permite organizar datos en varias dimensiones y acceder a ellos utilizando un índice por cada dimensión.