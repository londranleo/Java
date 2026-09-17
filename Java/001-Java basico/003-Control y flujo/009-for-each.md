## `for-each`

`for-each` es una forma de recorrer los elementos de una **colección o array uno por uno**, sin tener que controlar directamente sus índices.

Su estructura es:

```java
for (tipo elemento : colección) {
    // código
}
```

En cada repetición, Java obtiene el siguiente elemento de la colección y lo asigna a la variable indicada después del tipo.

Por ejemplo:

```java
int[] numeros = {10, 20, 30};

for (int numero : numeros) {
    System.out.println(numero);
}
```

El bucle recorrerá `10`, después `20` y finalmente `30`.

A diferencia del `for` tradicional, en `for-each` **no trabajamos directamente con un contador o índice**. Java se encarga de avanzar por los elementos.

Esto hace que sea especialmente útil cuando **solo necesitamos acceder a cada elemento**, pero no necesitamos conocer su posición.

Por ejemplo, si necesitamos saber el índice de cada elemento, modificar determinadas posiciones o recorrer solo una parte del array, un `for` tradicional puede ser más apropiado.

La variable utilizada para representar el elemento contiene el valor correspondiente a la iteración actual. Si se trata de objetos, la variable contiene una **referencia al objeto**, por lo que modificar el objeto puede afectar al objeto original; reasignar la variable, en cambio, no cambia el elemento almacenado en la colección.

>`for-each` permite recorrer los elementos de un array o colección directamente, obteniendo cada elemento uno por uno sin tener que gestionar manualmente los índices.