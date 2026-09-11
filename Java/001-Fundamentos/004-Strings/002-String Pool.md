# String Pool

El **String Pool** es una zona especial de memoria que Java utiliza para almacenar y reutilizar los `String` creados directamente mediante comillas dobles (literales de texto), en lugar de crear un objeto nuevo cada vez que aparece el mismo texto en el código.

Cuando se crea un `String` de esta forma, Java primero comprueba si ya existe en el String Pool un texto con exactamente el mismo contenido. Si existe, la nueva variable apunta al mismo objeto que ya estaba almacenado, en lugar de crear uno nuevo. Si no existe, Java crea el objeto, lo guarda en el String Pool y la variable apunta a él.

```java
String a = "Hola";
String b = "Hola";
```

En este ejemplo, `a` y `b` no son dos objetos distintos con el mismo contenido, sino que ambos apuntan al mismo objeto dentro del String Pool, ya que el texto `"Hola"` es idéntico en los dos casos.

Este comportamiento existe porque el texto es uno de los tipos de datos más utilizados en un programa, y muchas veces se repiten los mismos valores. Reutilizar el mismo objeto en lugar de crear uno nuevo cada vez ahorra memoria y mejora el rendimiento.

El String Pool solo aplica a los `String` creados como literales entre comillas. Los `String` creados de otras formas no se benefician automáticamente de este mecanismo, y su comportamiento respecto a la reutilización de memoria es distinto.