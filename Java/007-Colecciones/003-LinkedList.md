## `LinkedList`

`LinkedList` es otra implementación de `List`. A diferencia de `ArrayList`, está diseñada como una **lista enlazada**, donde los elementos están conectados entre sí mediante enlaces.

```java
List<String> nombres = new LinkedList<>();
```

Puedes utilizar los mismos métodos básicos de `List`:

```java
nombres.add("Ana");
nombres.add("Luis");
nombres.add("Carlos");

String nombre = nombres.get(1);

nombres.set(1, "Pedro");

nombres.remove(0);
```

### ¿Cómo funciona internamente?

En un `ArrayList`, los elementos están organizados sobre una estructura basada en un array:

```java
ArrayList

[ Ana ][ Luis ][ Carlos ][ ... ]
   0      1        2
```

En un `LinkedList`, cada elemento está dentro de un **nodo** que mantiene enlaces con otros nodos:

```java
[ Ana ] ⇄ [ Luis ] ⇄ [ Carlos ]
```

Cada nodo conoce qué elemento contiene y qué nodo está conectado antes y después.

Por eso, `LinkedList` puede ser especialmente útil cuando necesitamos **insertar o eliminar elementos en determinadas posiciones** con frecuencia.

### `ArrayList` vs `LinkedList`

La diferencia fundamental está en cómo almacenan los elementos:

|                            | `ArrayList`    | `LinkedList`                                       |
| -------------------------- | -------------- | -------------------------------------------------- |
| Estructura                 | Estructura     | Lista enlazada                                     |
| Acceso por índice          | Array dinámico | Más lento                                          |
| Añadir al final            | Rápido         | Muy eficiente                                      |
| Insertar/eliminar en medio | Muy eficiente  | Puede ser eficiente una vez localizada la posición |
| Uso habitual               | Más común      | Para casos específicos                             |

Por ejemplo, acceder directamente al elemento `500`:

```java
lista.get(500);
```

es más adecuado en `ArrayList`, porque puede acceder directamente a esa posición.

En `LinkedList`, para llegar a una posición concreta normalmente tiene que **recorrer los nodos hasta encontrarla**.

### Algo importante

Aunque `LinkedList` puede ser mejor para determinadas inserciones y eliminaciones, **no significa que siempre sea más rápida que `ArrayList` para modificar listas**. Primero hay que localizar el elemento, y esa búsqueda también tiene un coste.

Por eso, en aplicaciones normales, **`ArrayList` suele ser la opción predeterminada** y `LinkedList` se utiliza cuando sus características concretas realmente aportan una ventaja.

> `LinkedList` almacena los elementos mediante nodos enlazados. Esto hace que el acceso mediante índice sea menos eficiente que en `ArrayList`, pero puede resultar útil para determinadas operaciones de inserción y eliminación.