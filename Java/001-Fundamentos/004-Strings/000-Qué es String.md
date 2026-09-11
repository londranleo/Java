# Qué es `String`

`String` es el tipo de dato que se utiliza en Java para representar **texto**. Cualquier secuencia de caracteres —una palabra, una frase, un nombre, una dirección— se almacena en Java utilizando este tipo.

Un valor de tipo `String` se escribe entre comillas dobles:

```java
String saludo = "Hola, mundo";
```

A diferencia de los tipos primitivos como `int` o `double`, que almacenan directamente un valor simple, `String` es una **clase**, y por tanto una variable de tipo `String` almacena un **objeto**. Este objeto representa y gestiona internamente la secuencia de caracteres que forma el texto.

Aunque técnicamente es un objeto, Java permite trabajar con `String` de una forma muy parecida a como se trabaja con los tipos primitivos: se puede crear directamente escribiendo el texto entre comillas, sin necesidad de utilizar la palabra `new`, y se puede asignar, comparar o mostrar con la misma naturalidad que un número o un valor lógico.

Una vez creado, el contenido de un `String` no puede modificarse: cualquier operación que parezca cambiar su texto en realidad crea un nuevo `String` con el resultado, dejando el original intacto.