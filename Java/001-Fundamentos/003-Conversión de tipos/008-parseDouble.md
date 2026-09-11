# parseDouble

`parseDouble` es un método de la clase `Double` que convierte un texto (`String`) en un valor numérico de tipo `double`. Al igual que `parseInt`, forma parte de las utilidades que ofrecen las clases envoltorio para trabajar con los tipos primitivos.

Se utiliza escribiendo `Double.parseDouble()` y pasando como argumento el texto que se quiere convertir:

```java
String texto = "9.75";
double numero = Double.parseDouble(texto);
```

Para que la conversión funcione correctamente, el texto debe representar un número decimal válido, utilizando el punto (`.`) como separador decimal, sin espacios, letras ni símbolos adicionales (salvo un signo `+` o `-` al principio si corresponde). Si el texto no cumple este formato, `parseDouble` lanza un error en tiempo de ejecución, concretamente una excepción de tipo `NumberFormatException`, indicando que el texto no se pudo interpretar como un número.

A diferencia de `parseInt`, `parseDouble` también acepta textos que representen números enteros (por ejemplo, `"10"`), ya que un número entero es un valor decimal válido sin parte fraccionaria.