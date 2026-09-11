# Sufijos

Un **sufijo** es una letra que se añade al final de un literal numérico para indicar explícitamente a qué tipo de dato pertenece ese valor. Java necesita esta información porque, por defecto, interpreta los literales enteros como `int` y los literales con decimales como `double`; el sufijo permite indicar que se trata de un tipo distinto.

Los sufijos disponibles son:

| Sufijo   | Tipo   |
|----------|--------|
| `L` o `l`| long   |
| `F` o `f`| float  |
| `D` o `d`| double |

```java
long poblacion = 8000000000L;
float altura = 1.75f;
double peso = 68.5d;
```

En el caso de `double`, el sufijo `d` es opcional, ya que Java ya interpreta los literales decimales como `double` por defecto. En cambio, en `long` y `float` el sufijo sí es necesario, porque sin él Java trataría el literal como `int` o como `double`, respectivamente, lo que podría causar un error si el valor no encaja en ese tipo.

Se recomienda usar la letra mayúscula `L` en lugar de `l` en el caso de `long`, ya que la minúscula puede confundirse fácilmente con el número `1` al leer el código.