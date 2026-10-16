Los objetos `String` en Java son **inmutables**. Esto significa que, una vez creado un objeto `String`, **su contenido no puede modificarse**.

Cuando realizamos una operación que parece modificar una cadena, Java no cambia el objeto original. En su lugar, se crea **otra cadena con el nuevo contenido**, y la variable puede pasar a hacer referencia a esa nueva cadena. 

```java
String cadena1 = "Hola";
// No se modifica la cadena, se crea una nueva
cadena1 = "Adios";
```

