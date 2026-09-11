# Overflow

El **overflow** (desbordamiento) ocurre cuando el resultado de una operación supera el rango máximo (o mínimo) que un tipo de dato numérico puede almacenar. Como el tipo no tiene espacio suficiente para representar ese valor, el resultado no se descarta ni genera un error: en su lugar, el valor "da la vuelta" y continúa desde el otro extremo del rango.

```java
int numero = 2147483647; // valor máximo de int
numero = numero + 1;
System.out.println(numero); // -2147483648
```

En este ejemplo, al sumar 1 al valor máximo de `int`, el resultado no cabe en el rango permitido, por lo que el contador vuelve al valor mínimo en lugar de aumentar.

Este comportamiento ocurre de forma silenciosa: Java no avisa ni lanza ningún error cuando sucede, por lo que puede provocar resultados incorrectos difíciles de detectar si no se tiene en cuenta el rango del tipo utilizado.

El mismo fenómeno puede darse tanto por exceso (superar el valor máximo) como por defecto (bajar del valor mínimo), y afecta a cualquier tipo numérico entero según su tamaño en bits.