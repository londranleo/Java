## Casting

El **casting** es la conversión explícita de un valor de un tipo de dato a otro tipo compatible.

Se utiliza cuando queremos indicarle a Java que trate un valor como un **tipo diferente** al que tiene actualmente.

La sintaxis es:

```java
(tipo) valor
```

Por ejemplo:

```java
double numero = 10.5;
int entero = (int) numero;
```

El resultado será `10`. En este caso, la parte decimal se **descarta**, no se redondea.

### Casting entre tipos numéricos

El casting es especialmente habitual cuando trabajamos con tipos numéricos diferentes.

Por ejemplo:

```java
double → int
```

puede provocar una **pérdida de información**, porque `int` no puede almacenar decimales.

En cambio:

```java
int → double
```

puede realizarse sin perder el valor numérico, porque `double` puede representar valores enteros además de decimales.

Java realiza algunas conversiones automáticamente cuando son seguras. A esto se le llama **conversión implícita** o _widening_. Cuando necesitamos indicar nosotros la conversión mediante `(tipo)`, hablamos de **casting explícito**.

### Casting de referencias

El casting también existe entre **tipos de referencia**, especialmente cuando trabajamos con herencia:

```java
Animal animal = new Perro();
Perro perro = (Perro) animal;
```

Aquí estamos indicando que la referencia `animal` debe tratarse como un `Perro`.

Este tipo de casting solo es válido si el objeto realmente puede tratarse como el tipo indicado. Si no es así, puede producirse una `ClassCastException`.

>el casting permite realizar una **conversión explícita de un tipo a otro**. En tipos numéricos puede provocar pérdida de información, mientras que en referencias permite cambiar el tipo con el que tratamos un objeto dentro de una jerarquía compatible.