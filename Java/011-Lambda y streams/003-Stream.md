### `Stream`

Un **`Stream`** es una herramienta de Java que permite **procesar los elementos de una fuente de datos de forma declarativa**, aplicando operaciones sobre ellos sin tener que controlar manualmente todo el proceso de recorrido.

Un `Stream` puede recibir elementos de una colección, un array u otras fuentes y aplicarles diferentes operaciones, como **filtrar, transformar, ordenar o agrupar**.

La idea fundamental es que un `Stream` describe **qué queremos hacer con los datos**, en lugar de centrarse en cómo recorrerlos paso a paso.

Por ejemplo:

```java
List<Integer> numeros = List.of(1, 2, 3, 4, 5);

numeros.stream()
       .filter(n -> n > 2)
       .forEach(System.out::println);
```

Conceptualmente:

```
Fuente de datos
      ↓
   Stream
      ↓
   operación
      ↓
   operación
      ↓
 resultado
```

Es importante entender que un `Stream` **no es una colección** y no almacena los elementos por sí mismo.

Una `List`, por ejemplo, **almacena datos**:

```java
List
→ contiene elementos
```

Mientras que un `Stream` **procesa datos**:

```java
Stream
→ procesa elementos
```

Además, crear un `Stream` normalmente **no modifica la colección original**. Las operaciones trabajan sobre los elementos que recibe el flujo y producen resultados según las operaciones aplicadas.

### Operaciones de un `Stream`

Las operaciones suelen dividirse conceptualmente en dos grupos:

**Operaciones intermedias** → transforman el Stream y permiten continuar con más operaciones.

```
filter
map
sorted
```

**Operación terminal** → finaliza el procesamiento y produce un resultado o efecto.

```
forEach
collect
count
```

Esto permite construir una especie de **cadena de procesamiento**:

```
datos
 ↓
filter
 ↓
map
 ↓
sorted
 ↓
collect
 ↓
resultado
```

Una característica importante es que muchas operaciones de Stream son **lazy (perezosas)**. Las operaciones intermedias normalmente no se ejecutan inmediatamente; Java espera hasta que se solicita una operación terminal para comenzar realmente el procesamiento.

>un `Stream` es una herramienta para **procesar datos mediante una secuencia de operaciones**, permitiendo expresar de forma declarativa qué queremos hacer con los elementos sin gestionar manualmente todo el recorrido.