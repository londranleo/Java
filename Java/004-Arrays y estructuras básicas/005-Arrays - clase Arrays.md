## `Arrays` - clase `Arrays`

La clase **`Arrays`** pertenece a `java.util` y proporciona métodos útiles para **trabajar con arrays**.

Un array por sí solo permite almacenar y acceder a elementos, pero la clase `Arrays` proporciona operaciones habituales para trabajar con ellos sin tener que implementarlas manualmente.

Algunas de sus operaciones principales son:

| Método                  | Función                                                           |
| ----------------------- | ----------------------------------------------------------------- |
| `Arrays.toString()`     | Convierte el contenido de un array en una representación de texto |
| `Arrays.sort()`         | Ordena los elementos                                              |
| `Arrays.binarySearch()` | Busca un elemento en un array ordenado                            |
| `Arrays.equals()`       | Compara el contenido de dos arrays                                |
| `Arrays.fill()`         | Rellena el array con un valor                                     |
| `Arrays.copyOf()`       | Crea una copia con el tamaño indicado                             |
| `Arrays.copyOfRange()`  | Copia una parte del array                                         |

Por ejemplo, para ordenar un array:

```java
int[] numeros = {30, 10, 20};

Arrays.sort(numeros);
```

Después de la operación, los elementos estarán ordenados.

Es importante entender que estos métodos **trabajan sobre arrays**, pero cada uno tiene un comportamiento diferente. Algunos modifican el array original, mientras que otros crean y devuelven un nuevo array.

Por ejemplo, `sort()` modifica el array que recibe, mientras que `copyOf()` devuelve una nueva copia.

También es importante distinguir `Arrays.equals()` de `==`. `Arrays.equals()` compara los **elementos de los arrays**, mientras que `==` utilizado con arrays comprueba si ambas variables hacen referencia al **mismo array**.

>`Arrays` es una clase de utilidad que proporciona operaciones comunes para trabajar con arrays, como ordenar, copiar, comparar, buscar y rellenar sus elementos.