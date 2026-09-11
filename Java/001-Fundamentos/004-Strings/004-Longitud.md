# Longitud

La longitud de un `String` es el número total de caracteres que contiene el texto. En Java, esta información se obtiene mediante el método `length()`, que se llama sobre el propio `String` y devuelve ese número en forma de valor entero (`int`).

```java
String texto = "Hola";
int longitud = texto.length();
```

En este ejemplo, `longitud` tendría el valor `4`, ya que el texto `"Hola"` está formado por cuatro caracteres.

Es importante tener en cuenta que la longitud cuenta todos los caracteres del texto, incluyendo espacios y signos de puntuación, y que el último índice válido de un `String` siempre corresponde a su longitud menos uno, ya que la numeración de los índices comienza en `0`.

Si el `String` está vacío (no contiene ningún carácter), su longitud es `0`.