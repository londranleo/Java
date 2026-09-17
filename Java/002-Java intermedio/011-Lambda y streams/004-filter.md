### `filter`

`filter` es una **operación intermedia de un `Stream`** que permite seleccionar únicamente los elementos que **cumplen una determinada condición**.

La idea es sencilla: el `Stream` recibe una colección de elementos y `filter` comprueba cada elemento mediante una condición. Los elementos que cumplen la condición **continúan en el Stream** y los que no la cumplen **son descartados**.

```java
List<Integer> numeros = List.of(1, 2, 3, 4, 5);

numeros.stream()
       .filter(n -> n > 3);
```

Conceptualmente:

```
1 → ❌
2 → ❌
3 → ❌
4 → ✅
5 → ✅

Resultado:
4, 5
```

`filter` recibe un **`Predicate`**, que es una interfaz funcional encargada de representar una condición que devuelve `true` o `false`.

```
Elemento
   ↓
Predicate
   ↓
¿cumple la condición?
   │
 ┌─┴─┐
 ↓   ↓
Sí   No
 ↓   ↓
pasa descarta
```

Como `filter` es una **operación intermedia**, no produce por sí misma el resultado final ni ejecuta necesariamente el procesamiento inmediatamente. Devuelve otro `Stream` sobre el que podemos continuar realizando operaciones.

```java
numeros.stream()
       .filter(n -> n > 3)
       .map(n -> n * 2);
```

Esto permite construir una **cadena de procesamiento**, donde primero seleccionamos los elementos que nos interesan y después podemos transformarlos.

Es importante entender que `filter` **no modifica la colección original**. Su función es determinar qué elementos continúan dentro del flujo.

>`filter` sirve para **seleccionar elementos de un `Stream` según una condición**. Si el elemento cumple el `Predicate`, continúa; si no, queda fuera del flujo.