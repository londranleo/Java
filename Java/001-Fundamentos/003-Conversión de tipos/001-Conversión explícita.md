# Conversión explícita

La conversión explícita es el proceso mediante el cual el programador indica manualmente que quiere cambiar el tipo de un valor a otro, escribiendo el tipo destino entre paréntesis delante del valor. A esta técnica también se le llama *casting*.

Es necesaria cuando se quiere convertir un valor de un tipo "más grande" a uno "más pequeño", ya que en ese caso existe riesgo de perder información (por ejemplo, parte de los decimales o dígitos que no caben en el tipo destino). Como esa pérdida de datos podría ser un error involuntario, Java no la realiza de forma automática y obliga a que sea el programador quien decida hacerlo de manera consciente.

```java
double numero = 9.75;
int resultado = (int) numero;
```

En este ejemplo, `numero` es un `double` con decimales. Al convertirlo a `int` mediante `(int)`, Java elimina la parte decimal y `resultado` queda con el valor `9`, descartando el `.75`.

La sintaxis general consiste en colocar el tipo deseado entre paréntesis justo antes del valor o variable que se quiere convertir:

```text
(tipoDestino) valor
```

Al ir de un tipo más grande a uno más pequeño, siempre existe la posibilidad de que el valor original no quepa completamente en el tipo destino, por lo que el resultado puede no coincidir con el valor esperado si no se tiene cuidado al aplicar esta conversión.