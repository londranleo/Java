# parseInt

`parseInt` es un método de la clase `Integer` que convierte un texto (`String`) en un valor numérico de tipo `int`. Forma parte de las llamadas clases envoltorio, que son clases que acompañan a los tipos primitivos y ofrecen utilidades relacionadas con ellos.

Se utiliza escribiendo `Integer.parseInt()` y pasando como argumento el texto que se quiere convertir:

```java
String texto = "120";
int numero = Integer.parseInt(texto);
```

Para que la conversión funcione correctamente, el texto debe representar un número entero válido, sin espacios, letras ni símbolos adicionales (salvo un signo `+` o `-` al principio si corresponde). Si el texto no cumple este formato, `parseInt` lanza un error en tiempo de ejecución, concretamente una excepción de tipo `NumberFormatException`, indicando que el texto no se pudo interpretar como un número.

`parseInt` es específico para el tipo `int`. Las demás clases envoltorio ofrecen métodos equivalentes para sus propios tipos, como `parseDouble` en la clase `Double` o `parseLong` en la clase `Long`.