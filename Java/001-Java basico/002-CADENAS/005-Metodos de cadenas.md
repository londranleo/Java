Los **métodos de cadenas** son operaciones que proporciona la clase `String` para **consultar, analizar o generar contenido a partir de una cadena**. Permiten trabajar con el texto sin tener que manipular directamente cada uno de sus caracteres.

Como `String` es un objeto, sus métodos se utilizan sobre una cadena mediante el operador `.`. Muchos de estos métodos **no modifican la cadena original**, debido a su inmutabilidad, sino que devuelven un resultado o una nueva cadena.

Entre los métodos más utilizados se encuentran:

- `length()` → devuelve la cantidad de caracteres de la cadena.
- `charAt()` → devuelve el carácter situado en un índice determinado.
- `toUpperCase()` → devuelve la cadena convertida a mayúsculas.
- `toLowerCase()` → devuelve la cadena convertida a minúsculas.
- `trim()` → elimina determinados espacios al principio y al final.
- `strip()` → elimina espacios en blanco según las reglas de Unicode.
- `replace()` → sustituye determinados caracteres o secuencias.
- `contains()` → comprueba si una cadena contiene una determinada secuencia.
- `startsWith()` → comprueba si comienza con una determinada secuencia.
- `endsWith()` → comprueba si termina con una determinada secuencia.
- `isEmpty()` → comprueba si la cadena tiene una longitud de `0`.
- `isBlank()` → comprueba si está vacía o contiene únicamente caracteres de espacio.
- `substring()` → obtiene una parte de la cadena.
- `indexOf()` → busca la posición de un carácter o una subcadena.
- `lastIndexOf()` → busca la última posición en la que aparece.
- `equals()` → compara el contenido de dos cadenas.
- `equalsIgnoreCase()` → compara el contenido ignorando mayúsculas y minúsculas.
- `compareTo()` → compara dos cadenas según su orden lexicográfico.

Por ejemplo:

```java
String texto = "Hola Java";

int longitud = texto.length();
String mayusculas = texto.toUpperCase();
```

Aquí `length()` devuelve información sobre la cadena, mientras que `toUpperCase()` devuelve otra cadena con el texto transformado. La cadena original `"Hola Java"` permanece sin modificar.

Es importante distinguir entre **métodos que devuelven información** y **métodos que generan un nuevo resultado**. Algunos devuelven un valor como `int` o `boolean`, mientras que otros devuelven otro `String`.

Además, muchos métodos de `String` pueden combinarse para realizar operaciones más complejas sobre el texto.

