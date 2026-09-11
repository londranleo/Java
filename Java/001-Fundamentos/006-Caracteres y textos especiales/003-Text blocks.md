# Text blocks

Los **text blocks** (bloques de texto) son una forma de escribir textos largos, especialmente los que ocupan varias líneas, sin necesidad de usar la secuencia de escape `\n` ni concatenar varios `String` con `+`. Se delimitan con triple comilla doble (`"""`).

```java
String texto = """
    Hola,
    este es un texto
    de varias líneas.
    """;
```

Cada salto de línea real dentro del bloque se interpreta automáticamente como un salto de línea en el texto resultante, por lo que no hace falta escribir `\n` manualmente. Esto hace que textos largos, como fragmentos de HTML, JSON, o mensajes con varias líneas, resulten mucho más legibles directamente en el código, ya que se ven tal y como se van a mostrar.

Dentro de un text block se pueden seguir utilizando otras secuencias de escape cuando sean necesarias (por ejemplo, `\"` o `\\`), pero ya no son obligatorias para las comillas dobles ni para los saltos de línea, ya que el propio bloque permite escribirlos con mayor libertad sin que se interpreten como el final del texto.