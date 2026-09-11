# valueOf

`valueOf` es un método que ofrecen las clases envoltorio (como `Integer`, `Double`, `Long`, entre otras) para convertir un texto (`String`) en un valor numérico, de forma similar a `parseInt` o `parseDouble`. La diferencia está en lo que devuelve cada uno: mientras que `parseInt` o `parseDouble` devuelven directamente un valor primitivo (`int`, `double`...), `valueOf` devuelve un **objeto** de la clase envoltorio correspondiente (`Integer`, `Double`...).

Se utiliza escribiendo el nombre de la clase envoltorio seguido de `.valueOf()`, pasando como argumento el texto a convertir:

```java
String texto = "42";
Integer numero = Integer.valueOf(texto);
```

Al igual que ocurre con `parseInt` y `parseDouble`, el texto debe tener un formato numérico válido para el tipo correspondiente; si no lo tiene, `valueOf` lanza una excepción de tipo `NumberFormatException`.

Aunque `numero` en el ejemplo es un objeto `Integer` y no un `int` primitivo, Java permite en la mayoría de los casos utilizarlo directamente como si fuera un `int` gracias a un mecanismo automático de conversión entre objetos envoltorio y tipos primitivos.