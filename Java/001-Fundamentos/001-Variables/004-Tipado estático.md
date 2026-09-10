# Tipado estático

Java es un lenguaje de **tipado estático**, lo que significa que el tipo de dato de cada variable se define en el momento de declararla y no puede cambiar durante toda la ejecución del programa.

Cuando declaras una variable indicando su tipo, por ejemplo:

```java
int edad = 25;
```

estás diciéndole a Java que `edad` va a contener siempre un número entero. A partir de ese momento, esa variable no puede guardar ningún otro tipo de dato, ni siquiera otro número que no sea entero, como uno con decimales.

El tipado estático se comprueba **antes de ejecutar el programa**, durante la compilación. Esto significa que si intentas guardar un valor de un tipo distinto al de la variable, Java detecta el error inmediatamente y no te deja compilar el código, evitando así errores que podrían aparecer más adelante mientras el programa se está ejecutando.

Esta forma de trabajar aporta seguridad y claridad: al leer el código, siempre sabes con certeza qué tipo de dato contiene cada variable, sin tener que adivinarlo ni comprobarlo durante la ejecución.

El tipado estático se diferencia del **tipado dinámico**, que utilizan otros lenguajes, donde una misma variable puede cambiar de tipo de dato libremente durante la ejecución del programa. Java no permite este comportamiento.