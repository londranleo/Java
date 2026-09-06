El **formateo de cadenas** consiste en construir un texto combinando una cadena de formato con diferentes valores, colocando cada valor en una posición determinada y, cuando es necesario, indicando **cómo debe representarse**.

Es especialmente útil cuando necesitamos crear mensajes que contienen información variable, como nombres, edades, precios, fechas o resultados.

En Java existen varias formas de realizar el formateo. Una de las más importantes es `String.format()`.

### `String.format()`

`String.format()` permite crear una nueva cadena a partir de un **texto de formato** y una serie de valores. Dentro del texto se utilizan **especificadores de formato** que indican dónde debe colocarse cada valor y cómo debe representarse.

```
String nombre = "Leo";
int edad = 22;

String mensaje = String.format("Me llamo %s y tengo %d años", nombre, edad);
```

El resultado será:

```
Me llamo Leo y tengo 22 años
```

En este caso:

- `%s` representa un valor de texto (`String`).
- `%d` representa un número entero.
- Los valores proporcionados después de la cadena de formato se colocan en los especificadores correspondientes y **en el mismo orden**.

Existen diferentes especificadores dependiendo del tipo de valor que queramos representar:

|Especificador|Uso|
|---|---|
|`%s`|Texto|
|`%d`|Número entero|
|`%f`|Número decimal|
|`%c`|Carácter|
|`%b`|Booleano|
|`%n`|Salto de línea|

El formateo también permite **controlar la representación de los valores**, por ejemplo, indicando cuántos decimales debe mostrar un número.

```
double precio = 19.995;

String resultado = String.format("%.2f €", precio);
```

El resultado será:

```
20.00 €
```

Aquí `%.2f` indica que el número decimal debe representarse mostrando **dos cifras después del punto decimal**.

### `formatted()`

Los objetos `String` también disponen del método `formatted()`, que permite realizar el formateo utilizando la propia cadena como plantilla.

Conceptualmente, cumple una función similar a `String.format()`, pero se utiliza directamente sobre el `String`.

### Formateo mediante `printf()`

`System.out.printf()` utiliza los mismos conceptos de especificadores de formato, pero en lugar de crear y devolver una cadena formateada, **la escribe directamente en la consola**.

Esto permite controlar cómo se muestran los valores sin tener que almacenar previamente el resultado en una variable.

>**Idea clave:** el formateo de cadenas permite construir texto dinámico de forma controlada. Los especificadores de formato indican dónde se colocan los valores y cómo deben representarse, permitiendo controlar aspectos como el tipo de dato, los decimales o el formato de salida.