# StringBuilder

`StringBuilder` es una clase de Java pensada para construir y modificar texto de forma eficiente. Pertenece al paquete `java.lang`, por lo que puede utilizarse directamente sin necesidad de importarla.

A diferencia de `String`, un objeto `StringBuilder` es **mutable**: se puede añadir, insertar, eliminar o modificar texto sobre el mismo objeto, sin crear uno nuevo en cada cambio.

```java
StringBuilder sb = new StringBuilder("Java");
sb.append(" es potente");
// sb contiene: "Java es potente"
```

Sus métodos **no están sincronizados**, lo que significa que no está preparado para que varios hilos (partes del programa que se ejecutan al mismo tiempo) lo modifiquen simultáneamente de forma segura. Al no incluir esa protección extra, `StringBuilder` resulta más rápido que otras alternativas equivalentes que sí la incluyen.

En la práctica, esto no supone ningún inconveniente en la mayoría de programas, ya que normalmente solo una parte del código trabaja con el objeto a la vez. Por este motivo, `StringBuilder` es la opción más utilizada para construir o modificar texto de forma habitual.