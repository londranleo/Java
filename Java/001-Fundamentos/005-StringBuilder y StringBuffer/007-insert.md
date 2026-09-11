# insert

El método `insert` añade contenido en una posición concreta del texto, desplazando el resto de caracteres hacia la derecha para hacer sitio.

```java
StringBuilder sb = new StringBuilder("Java potente");
sb.insert(4, " es");
// sb contiene: "Java es potente"
```

La posición se indica mediante un índice, donde el primer carácter del texto ocupa la posición 0. El contenido insertado se coloca justo antes del carácter que ocupaba esa posición.

Al igual que `append`, puede recibir distintos tipos de datos (texto, números, caracteres, etc.), convirtiéndolos automáticamente a texto, y también devuelve el propio objeto tras la modificación, por lo que permite encadenar llamadas.

```java
StringBuilder sb = new StringBuilder("Tengo años");
sb.insert(6, "25 ");
// sb contiene: "Tengo 25 años"
```