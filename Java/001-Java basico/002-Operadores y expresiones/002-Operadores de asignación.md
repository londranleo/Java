## Operadores de asignación

Los **operadores de asignación** se utilizan para **asignar un valor a una variable**. El operador básico es `=`, que toma el valor situado a la derecha y lo asigna a la variable situada a la izquierda.

```java
int edad = 22;
```

En este caso, `22` es el valor que se asigna a `edad`.

Es importante no confundir `=` con una igualdad matemática. En programación, `=` representa una **asignación**: la variable pasa a contener el resultado de la expresión que está a la derecha.

La asignación también puede realizarse después de haber declarado la variable:

```java
int edad;
edad = 22;
```

### Asignación combinada

Java proporciona operadores que combinan una operación aritmética con una asignación:

|Operador|Equivalencia|
|---|---|
|`+=`|`a = a + valor`|
|`-=`|`a = a - valor`|
|`*=`|`a = a * valor`|
|`/=`|`a = a / valor`|
|`%=`|`a = a % valor`|

Por ejemplo:

```java
int puntos = 10;
puntos += 5;
```

Después de la operación, `puntos` contiene `15`.

Estos operadores son una forma abreviada de realizar una operación utilizando el valor que ya tiene la propia variable.

### Asignación y expresiones

La parte derecha de una asignación puede ser simplemente un valor, otra variable o una expresión completa. Java primero **evalúa la expresión de la derecha** y posteriormente asigna el resultado a la variable de la izquierda.

```java
int resultado = 10 + 5 * 2;
```

Primero se evalúa la expresión siguiendo las reglas de los operadores y después el resultado se asigna a `resultado`.

El tipo del valor obtenido debe ser compatible con el tipo de la variable a la que se asigna. Si no existe una conversión válida, el compilador producirá un error.
