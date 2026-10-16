## Recorrido de un array

**Recorrer un array** significa acceder a sus elementos **uno por uno**, normalmente para leerlos, modificarlos o realizar alguna operación con ellos.

La forma más habitual de recorrer un array es mediante un bucle `for`. Como los índices empiezan en `0`, podemos utilizar una variable para avanzar desde el primer índice hasta el último.

```java
int[] numeros = {10, 20, 30};

for (int i = 0; i < numeros.length; i++) {
    System.out.println(numeros[i]);
}
```

En cada vuelta, `i` representa el **índice del elemento actual**. Al utilizar `numeros[i]`, obtenemos el valor almacenado en esa posición.

La condición `i < numeros.length` es importante porque `length` indica cuántos elementos tiene el array, mientras que el último índice es `length - 1`.

También podemos recorrer un array mediante `for-each`, cuando no necesitamos trabajar directamente con los índices:

```java
for (int numero : numeros) {
    System.out.println(numero);
}
```

La diferencia principal es:

```
for       → permite controlar el índice
for-each  → trabaja directamente con cada elemento
```

Recorrer un array es una operación fundamental porque muchas veces necesitamos procesar **todos sus elementos** para buscar un valor, calcular un resultado, modificar datos o mostrarlos.

> recorrer un array consiste en acceder a sus elementos de forma secuencial. Podemos hacerlo con `for` cuando necesitamos controlar los índices o con `for-each` cuando solo necesitamos trabajar con los elementos.