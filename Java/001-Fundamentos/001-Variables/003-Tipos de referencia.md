# Tipos de referencia

Los tipos de referencia son tipos de datos en Java que no guardan el valor directamente dentro de la variable, como sí hacen los tipos primitivos.

En su lugar, la variable guarda una referencia: una especie de indicación de en qué parte de la memoria está guardado el valor real.

```java
String nombre = "Ana";
```

En este caso, `nombre` no contiene el texto "Ana" en sí, sino la referencia que señala dónde está guardado ese texto en la memoria.

Todo lo que no sea un tipo primitivo en Java (como los textos, los objetos creados con `new`, o los arrays) es un tipo de referencia.
