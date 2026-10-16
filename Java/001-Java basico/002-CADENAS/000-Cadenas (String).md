Una **cadena de caracteres** es una secuencia de caracteres utilizada para representar texto. En Java, las cadenas se representan mediante la clase `String`. Las cadeanas se utilizan para almacemar y manipular texto.

A diferencia de los tipos primitivos, `String` es un **tipo de referencia**, ya que representa objetos.

```java
String cadena1 = "Hola";

String cadena2 = new String("Mundo");

String cadena3 = cadena1 + " " + cadena2;

// Cadena multiples lineas 
var cadena4 = """ 
	este 
	es un texto 
	multilinea
	""";
```

Una característica fundamental de `String` es que sus objetos son **inmutables**. Esto significa que, una vez creado un objeto `String`, su contenido no puede modificarse directamente. Las operaciones que parecen modificar una cadena producen en realidad otra cadena con el nuevo contenido.



