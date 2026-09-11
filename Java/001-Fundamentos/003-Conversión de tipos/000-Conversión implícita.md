# Conversión implícita

La conversión implícita es el proceso mediante el cual Java cambia automáticamente el tipo de un valor a otro tipo compatible, sin que el programador tenga que indicarlo de forma explícita en el código.

Esto ocurre cuando se asigna o se opera con un valor de un tipo "más pequeño" (que ocupa menos espacio en memoria) en un contexto donde se espera un tipo "más grande" (que ocupa más espacio). Como el tipo más grande puede representar todos los valores posibles del tipo más pequeño sin perder información, Java realiza el cambio automáticamente y de forma segura.

```java
int numero = 10;
double resultado = numero;
```

En este ejemplo, `numero` es un `int`, pero se asigna a una variable `double`. Java convierte automáticamente el valor entero a decimal, sin que sea necesario escribir nada adicional.

Este tipo de conversión sigue un orden concreto entre los tipos numéricos, desde los que ocupan menos espacio hasta los que ocupan más:

```text
byte → short → int → long → float → double
```

Un valor puede convertirse automáticamente hacia cualquier tipo situado a su derecha en esta secuencia, porque ese tipo siempre puede contener los mismos valores sin pérdida de precisión.

La conversión implícita también sucede al mezclar tipos numéricos distintos en una misma operación: Java convierte automáticamente el valor del tipo más pequeño al tipo más grande antes de realizar el cálculo, y el resultado final adopta ese tipo más grande.