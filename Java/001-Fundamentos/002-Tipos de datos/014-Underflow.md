# Underflow

El **underflow** es un fenómeno que ocurre en los tipos de dato con decimales (`float` y `double`) cuando el resultado de una operación es un número tan pequeño, tan cercano a cero, que el tipo no tiene precisión suficiente para representarlo con exactitud. En ese caso, el valor se redondea a cero en lugar de mostrar el resultado real.

```java
double numero = 1.0e-310;
numero = numero / 1000;
System.out.println(numero); // 0.0
```

En este ejemplo, el resultado de la división es un número tan diminuto que queda fuera del límite de precisión que `double` puede representar, por lo que Java lo aproxima a `0.0`.

Al igual que el overflow, el underflow ocurre de forma silenciosa: Java no lanza ningún error ni aviso cuando sucede, lo que puede generar resultados incorrectos si no se tiene en cuenta la precisión limitada de los tipos con decimales.