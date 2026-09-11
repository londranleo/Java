# StringBuffer

`StringBuffer` es una clase de Java que, al igual que `StringBuilder`, permite construir y modificar texto de forma eficiente sobre el mismo objeto, sin necesidad de crear uno nuevo en cada cambio. Pertenece al paquete `java.lang`, por lo que puede utilizarse directamente sin necesidad de importarla.

```java
StringBuffer sb = new StringBuffer("Java");
sb.append(" es potente");
// sb contiene: "Java es potente"
```

La diferencia clave frente a `StringBuilder` es que sus métodos **están sincronizados**. Esto significa que `StringBuffer` está preparado para que varios hilos (partes del programa que se ejecutan al mismo tiempo) puedan modificar el mismo objeto de forma segura, evitando que se produzcan errores o datos corruptos por accesos simultáneos al mismo texto.

Esa protección adicional tiene un coste: al tener que controlar el acceso entre hilos, `StringBuffer` resulta más lento que `StringBuilder`. Por eso solo se recomienda utilizarlo cuando realmente exista la posibilidad de que varios hilos trabajen sobre el mismo objeto al mismo tiempo.