La **búsqueda de subcadenas** consiste en localizar una determinada secuencia de caracteres dentro de otra cadena. Permite comprobar si un texto contiene una palabra o fragmento concreto y, además, conocer la posición en la que aparece.

En Java, `String` proporciona principalmente los métodos `contains()`, `indexOf()` y `lastIndexOf()` para realizar este tipo de operaciones.

`contains()` se utiliza cuando únicamente necesitamos saber **si una subcadena está presente**. Devuelve un valor `boolean`: `true` si la encuentra y `false` si no está presente.

```java
String texto = "Estoy aprendiendo Java";

texto.contains("Java"); // true
```

`indexOf()` permite obtener **la posición de la primera aparición** de un carácter o subcadena. Si no encuentra el contenido buscado, devuelve `-1`.

```java
String texto = "Java es un lenguaje";

int posicion = texto.indexOf("lenguaje"); //11
```

`lastIndexOf()` funciona de forma similar, pero busca **la última aparición** del contenido.

La búsqueda distingue entre mayúsculas y minúsculas. Por ejemplo, `"Java"` y `"java"` no se consideran la misma subcadena en una búsqueda normal.

Estos métodos no modifican la cadena original. Únicamente **consultan su contenido y devuelven información sobre él**.


