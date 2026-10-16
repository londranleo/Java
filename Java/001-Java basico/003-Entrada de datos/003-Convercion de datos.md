La **conversión de datos** consiste en transformar un valor de un tipo de dato a otro. En Java es necesaria cuando queremos utilizar un valor en un contexto que requiere un tipo diferente.

La conversión puede producirse de forma **implícita** o **explícita**, dependiendo de los tipos que intervienen y de si Java puede realizar la conversión de manera segura.

### Conversión implícita

Se produce cuando Java puede convertir automáticamente un tipo a otro compatible sin que tengamos que indicarlo.

Esto ocurre principalmente cuando se pasa de un tipo numérico con menor capacidad de representación a otro con mayor capacidad.

```java
int numero = 10;
double decimal = numero;
```

El `int` se convierte automáticamente en `double`.

Este tipo de conversión normalmente no requiere una indicación adicional porque el tipo de destino puede representar los valores del tipo de origen sin una pérdida habitual de información.

### Conversión explícita

Se utiliza cuando Java no puede realizar la conversión automáticamente o cuando queremos indicar expresamente el tipo al que debe convertirse el valor.

Para ello se utiliza un **casting**, escribiendo el tipo de destino entre paréntesis:

```java
double precio = 19.99;
int entero = (int) precio;
```

En este caso, la conversión de `double` a `int` puede provocar **pérdida de información**, ya que la parte decimal no puede mantenerse en un `int`.

El casting no redondea automáticamente el número; elimina la parte decimal.


### Conversión entre `String` y otros tipos

La conversión de datos también puede implicar texto. Un `String` que contiene un número no es lo mismo que un número.

```java
String numero = "25";
int numero1 = 25;
```

Para convertir texto a un tipo numérico se utilizan métodos de las clases correspondientes, como `Integer.parseInt()` o `Double.parseDouble()`.

```java
String edadString = "22";
doubele edad = Double.parseDouble(edadString); //22.0
```


En sentido contrario, un valor puede convertirse en texto mediante métodos como `String.valueOf()`.

Por tanto, hay que diferenciar entre **convertir tipos numéricos entre sí** y **convertir texto que representa un valor en un tipo numérico**.

