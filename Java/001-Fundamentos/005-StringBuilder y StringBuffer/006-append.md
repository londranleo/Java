# append

El método `append` añade contenido al final del texto actual, modificando el mismo objeto.

```java
StringBuilder sb = new StringBuilder("Java");
sb.append(" es potente");
// sb contiene: "Java es potente"
```

Puede recibir distintos tipos de datos (texto, números, caracteres, booleanos, etc.), y los convierte automáticamente a texto antes de añadirlos.

```java
StringBuilder sb = new StringBuilder("Edad: ");
sb.append(25);
// sb contiene: "Edad: 25"
```

Es posible encadenar varias llamadas a `append` en una misma línea, ya que el método devuelve el propio objeto después de modificarlo.

```java
StringBuilder sb = new StringBuilder();
sb.append("Hola").append(" ").append("mundo");
// sb contiene: "Hola mundo"
```