### `sorted`

`sorted` es una **operación intermedia de un `Stream`** que permite **ordenar los elementos** del flujo según un determinado criterio.

A diferencia de `filter`, que selecciona elementos, y `map`, que los transforma, `sorted` **cambia el orden en el que los elementos serán procesados posteriormente**.

Por defecto, `sorted()` utiliza el **orden natural** de los elementos.

```
List<Integer> numeros = List.of(5, 2, 4, 1, 3);

numeros.stream()
       .sorted();
```

Conceptualmente:

```
Antes:
5 → 2 → 4 → 1 → 3

Después:
1 → 2 → 3 → 4 → 5
```

Para que Java pueda utilizar el orden natural, los elementos deben proporcionar una forma de determinar su orden, normalmente mediante `Comparable`.

También podemos proporcionar un **`Comparator`** cuando queremos utilizar un criterio diferente al orden natural.

```java
personas.stream()
        .sorted(Comparator.comparingInt(Persona::getEdad));
```

En este caso, los objetos `Persona` se ordenan según su edad.

```
Persona
   ↓
Comparator
   ↓
criterio de orden
   ↓
Stream ordenado
```

`sorted` es una **operación intermedia**, por lo que devuelve otro `Stream` y puede combinarse con otras operaciones.

```
filter
  ↓
map
  ↓
sorted
  ↓
operación terminal
```

Es importante diferenciar el orden del `Stream` del almacenamiento de la colección original. `sorted` **no reorganiza la colección original**; establece el orden de los elementos dentro del flujo que continúa procesándose.

>`sorted` permite **ordenar los elementos de un `Stream`** utilizando su orden natural o un `Comparator` que define un criterio de ordenación específico.