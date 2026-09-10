# final

`final` es una palabra que puedes poner delante de una variable para decir que su valor no se va cambiar nunca después de asignar el valor.


```java
final int edad = 10;
edad = 12; // esto da error, porque "edad" es final y no se puede cambiar
```

Si intentas cambiar el valor de una variable `final` más adelante en el código, Java te va a marcar un error y no te va a dejar hacerlo.

Se suele usar cuando quieres estar seguro de que ese valor va a seguir siendo siempre el mismo durante todo el programa.