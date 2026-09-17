### `collect`

`collect` es una **operación terminal de un `Stream`** que permite **recoger los elementos procesados y convertirlos en una estructura o resultado final**.

Hasta ahora hemos visto operaciones como `filter`, `map` y `sorted`, que transforman el flujo pero **devuelven otro `Stream`**. `collect` marca normalmente el momento en el que dejamos de trabajar con el flujo y queremos obtener un resultado.

```java
List<String> nombres = personas.stream()
        .map(Persona::getNombre)
        .collect(Collectors.toList());
```

Conceptualmente:

```
Colección
    ↓
  Stream
    ↓
   map
    ↓
 elementos transformados
    ↓
 collect
    ↓
 resultado final
```

La parte importante es que `collect` **no determina por sí mismo cómo queremos almacenar el resultado**. Utiliza un mecanismo llamado **`Collector`**, que define cómo deben acumularse los elementos.

Por eso podemos utilizar `collect` para obtener diferentes tipos de resultados:

```
Stream
  ↓
collect
  ├── List
  ├── Set
  ├── Map
  └── otros resultados
```

También puede utilizarse para realizar operaciones de agrupación, partición o combinación de elementos, por lo que `collect` es una de las operaciones más importantes cuando trabajamos con Streams.

Por ejemplo, podemos transformar una colección y después recoger el resultado en una lista:

```java
List<Integer> mayores = numeros.stream()
        .filter(n -> n > 10)
        .collect(Collectors.toList());
```

Es importante distinguir entre **`Stream` y `Collection`**:

```
Collection
→ almacena los elementos

Stream
→ procesa los elementos

collect
→ recoge el resultado del procesamiento
```

`collect` es una **operación terminal**, por lo que una vez ejecutada, ese procesamiento del `Stream` ha terminado.

>`collect` permite **recoger el resultado de un `Stream`**, transformando el flujo procesado en una estructura o resultado final mediante un `Collector`.