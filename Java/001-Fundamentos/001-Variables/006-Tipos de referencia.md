# Tipos de referencia

Los tipos de referencia son los tipos de datos en Java que no almacenan el valor directamente en la variable, sino la dirección de memoria donde ese valor está guardado. En lugar de contener el dato en sí, la variable contiene una especie de "puntero" que indica dónde encontrarlo.

Cuando declaras una variable de tipo de referencia, Java crea el objeto real en una zona de memoria distinta, y la variable simplemente guarda una referencia (una dirección) que apunta hacia ese objeto. Por eso, a este tipo de variables también se las llama "variables de objeto".

```java
String nombre = "Ana";
```

Aquí `nombre` no contiene directamente el texto `"Ana"`. Contiene una referencia que apunta al lugar de la memoria donde ese texto está realmente almacenado.

Una consecuencia importante de esto es que dos variables de tipo de referencia pueden apuntar al mismo objeto en memoria. Si una variable modifica el contenido del objeto al que apunta, esa modificación se refleja también en la otra variable, porque ambas están señalando al mismo lugar.

Los tipos de referencia incluyen todas las clases de Java, ya sean las que vienen incluidas en el lenguaje (como `String`) o las que un programador crea por su cuenta. Se diferencian de los tipos primitivos en que estos últimos guardan el valor directamente, sin necesidad de apuntar a ningún otro lugar de la memoria.

Una variable de tipo de referencia que no apunta a ningún objeto tiene el valor especial `null`, que indica que no hace referencia a nada.