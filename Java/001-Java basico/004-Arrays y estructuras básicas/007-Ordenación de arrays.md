## Ordenación de arrays

La **ordenación** consiste en organizar los elementos de un array siguiendo un determinado orden, normalmente de **menor a mayor**.

Java proporciona el método `Arrays.sort()` para realizar esta operación.

```java
int[] numeros = {30, 10, 20};

Arrays.sort(numeros);
```

Después de ordenarlo:

```java
10, 20, 30
```

`Arrays.sort()` **modifica el array original**. No crea otro array con los elementos ordenados.

También puede utilizarse con otros tipos de datos, como `String`. En ese caso, los elementos se ordenan siguiendo el orden natural definido para ese tipo.

La ordenación también puede realizarse sobre una **parte del array**, indicando un índice inicial y uno final. El índice final no forma parte de la zona que se ordena.

```
Arrays.sort(numeros, 1, 3);
```

Esto permite ordenar únicamente los elementos comprendidos entre esas posiciones.

Java también permite utilizar `Arrays.sort()` con arrays de objetos y proporcionar un `Comparator` para definir **cómo deben ordenarse**. Esto será especialmente importante cuando estudiemos objetos y colecciones.

>ordenar un array significa reorganizar sus elementos según un criterio. `Arrays.sort()` permite realizar esta operación y, por defecto, utiliza el orden natural de los elementos.