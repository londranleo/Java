# Mutabilidad

La mutabilidad es la capacidad de un objeto para cambiar su contenido después de haber sido creado, manteniéndose como el mismo objeto en memoria.

`StringBuilder` y `StringBuffer` son **mutables**: cuando se les añade, elimina o modifica texto, el objeto original se actualiza directamente, sin crear uno nuevo.

```java
StringBuilder sb = new StringBuilder("Hola");
sb.append(" mundo");
// Sigue siendo el mismo objeto "sb", ahora con el contenido "Hola mundo"
```

Esto contrasta con los objetos inmutables, como `String`, donde cualquier modificación obliga a crear un objeto nuevo en lugar de cambiar el existente. Gracias a la mutabilidad, `StringBuilder` y `StringBuffer` pueden realizar múltiples cambios sobre el mismo texto de forma más eficiente, sin generar objetos innecesarios en cada modificación.