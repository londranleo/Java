# Escape sequences

Algunos caracteres no se pueden escribir directamente dentro de un texto, bien porque tienen un significado especial dentro del propio código (como las comillas, que delimitan dónde empieza y termina un texto), o porque no son caracteres visibles (como un salto de línea o una tabulación). Para poder incluirlos, Java utiliza las **secuencias de escape**.

Una secuencia de escape es una combinación que empieza con una barra invertida (`\`) seguida de un carácter, y que Java interpreta como un carácter especial en lugar de como texto literal.

```java
String texto = "Línea 1\nLínea 2";
```

Java incluye varias secuencias de escape predefinidas, cada una representando un carácter especial distinto: saltos de línea, tabulaciones, comillas, barras invertidas, retornos de carro, entre otras. Todas ellas se utilizan de la misma forma: se escriben dentro del texto en el lugar donde se necesita el carácter especial, y Java las sustituye automáticamente por su significado real al procesar el texto.

```java
String frase = "Ella dijo \"hola\"\t(en voz baja)";
```