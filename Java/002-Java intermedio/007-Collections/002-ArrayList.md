## `ArrayList`

`ArrayList` es una **implementación de `List`** que permite almacenar elementos en una colección cuyo tamaño puede cambiar durante la ejecución.

Internamente utiliza una estructura basada en un **array**, pero se encarga automáticamente de gestionar su tamaño cuando necesitamos almacenar más elementos.

```java
List<String> nombres = new ArrayList<>();
```

Podemos añadir elementos con `add()`:

```java
nombres.add("Ana");
nombres.add("Luis");
nombres.add("Carlos");
```

La lista mantiene el orden en el que añadimos los elementos y cada uno tiene una posición:

```java
índice:   0       1        2
          ↓       ↓        ↓
        Ana     Luis     Carlos
```

Podemos acceder a un elemento mediante `get()`:

```java
String nombre = nombres.get(1);
```

También podemos modificarlo con `set()`:

```java
nombres.set(1, "Pedro");
```

Y eliminarlo con `remove()`:

```java
nombres.remove(0);
```

El tamaño actual se obtiene mediante `size()`:

```java
int cantidad = nombres.size();
```

Una diferencia importante respecto a un array es que un `ArrayList` **no tiene un tamaño fijo**. Podemos añadir y eliminar elementos durante la ejecución:

```java
Array
→ tamaño establecido al crearlo

ArrayList
→ tamaño variable
```

`ArrayList` permite elementos duplicados:

```java
nombres.add("Ana");
nombres.add("Ana");
```

Ambos elementos pueden existir en la lista y ocupar posiciones diferentes.

También podemos recorrerlo mediante un `for-each`:

```java
for (String nombre : nombres) {
    System.out.println(nombre);
}
```

>`ArrayList` es una implementación de `List` basada en un array que permite almacenar una cantidad variable de elementos, mantener su orden, acceder mediante índices y añadir, modificar o eliminar elementos.