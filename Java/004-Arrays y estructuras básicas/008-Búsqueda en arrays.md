## Búsqueda en arrays

La **búsqueda** en un array consiste en comprobar si un determinado valor se encuentra dentro de él y, dependiendo del método utilizado, obtener su posición.

Una forma sencilla es recorrer el array y comparar cada elemento con el valor que buscamos.

Java también proporciona métodos específicos en la clase `Arrays`.

### `Arrays.binarySearch()`

`binarySearch()` permite buscar un elemento dentro de un array **ordenado**.

```java
int[] numeros = {10, 20, 30, 40};

int posicion = Arrays.binarySearch(numeros, 30);
```

El resultado será el índice donde se encuentra `30`.

Una característica importante es que el array debe estar **ordenado previamente** para que `binarySearch()` funcione correctamente.

Si el elemento no se encuentra, el método devuelve un valor negativo.

### Búsqueda recorriendo el array

También podemos realizar una búsqueda manual recorriendo los elementos:

```java
for (int numero : numeros) {
    if (numero == 30) {
        // encontrado
    }
}
```

Esta forma no requiere que el array esté ordenado, pero debemos comprobar los elementos uno por uno.

La diferencia principal es:

```java
Recorrido → comprueba los elementos uno por uno
binarySearch() → busca rápidamente en un array ordenado
```

