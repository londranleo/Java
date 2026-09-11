# Unicode

Unicode es un estándar que asigna un **número único** a cada carácter posible: letras, dígitos, símbolos, emojis, y caracteres de prácticamente cualquier idioma del mundo. Gracias a este estándar, cada carácter tiene siempre el mismo código sin importar el sistema, programa o idioma en el que se utilice.

En Java, este estándar es precisamente lo que hay detrás del tipo `char`: cada `char` almacena internamente el código Unicode del carácter que representa, en lugar del carácter en sí.

```java
char letra = 'ñ';
```

Además de escribir el carácter directamente, es posible representarlo mediante su código Unicode en hexadecimal, usando la notación `\uXXXX`:

```java
char letra = '\u00F1'; // representa 'ñ'
```

Gracias a Unicode, Java puede trabajar de forma nativa con letras acentuadas, símbolos, caracteres de idiomas como el chino o el árabe, e incluso ciertos emojis, sin necesidad de configuraciones adicionales, ya que todos ellos están contemplados dentro del propio estándar.