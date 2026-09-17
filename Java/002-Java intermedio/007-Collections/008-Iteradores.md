# Iterator

Un **`Iterator`** es un objeto que permite **recorrer los elementos de una colección uno por uno**, sin necesidad de acceder directamente a su estructura interna.

Su objetivo principal es proporcionar una forma **uniforme de recorrer colecciones**, especialmente aquellas en las que no existe un índice, como `Set`.

Un `Iterator` mantiene una posición dentro de la colección y permite avanzar progresivamente por sus elementos.

```java
Iterator<String> iterator = nombres.iterator();

while (iterator.hasNext()) {
    String nombre = iterator.next();
}
```

Los dos métodos fundamentales son:

- `hasNext()` → comprueba si quedan elementos por recorrer.
- `next()` → obtiene el siguiente elemento y avanza la posición del iterador.

Conceptualmente:

```java
Colección

[Ana] [Luis] [Carlos]
  ↑
  Iterator

hasNext() → ¿hay otro elemento?
next()    → obtiene el siguiente
```

Una característica importante es que el `Iterator` **separa la forma de recorrer una colección de la estructura concreta que utiliza internamente**. No necesitamos saber cómo están almacenados los elementos para recorrerlos.

También permite **eliminar elementos durante el recorrido** mediante `remove()`, de una forma controlada por el propio iterador. Esto es importante porque modificar directamente una colección mientras se está recorriendo puede provocar problemas como `ConcurrentModificationException`.

```java
Iterator<String> iterator = nombres.iterator();

while (iterator.hasNext()) {
    String nombre = iterator.next();

    if (nombre.equals("Ana")) {
        iterator.remove();
    }
}
```

`Iterator` puede utilizarse con diferentes colecciones, como `List` y `Set`, aunque cada colección puede tener internamente una forma diferente de almacenar sus elementos.

>[!Importante]
>`Iterator` proporciona una forma estándar de **recorrer una 
>colección elemento por elemento**, independientemente de cómo
> esté implementada internamente.