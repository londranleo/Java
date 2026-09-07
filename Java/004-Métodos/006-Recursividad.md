## Recursividad

La **recursividad** ocurre cuando un método **se llama a sí mismo** para resolver un problema.

La idea principal es dividir un problema en problemas más pequeños del mismo tipo. Cada llamada utiliza una versión más pequeña o sencilla del problema hasta llegar a una situación en la que ya no es necesario realizar otra llamada.

Para que una función recursiva pueda terminar necesita una **condición base**. Esta condición indica cuándo debe detenerse la recursión.

La estructura general es:

```java
tipo metodo(datos) {
    if (condicionBase) {
        return resultado;
    }

    return metodo(datosMasPequenos);
}
```

Por ejemplo:

```java
int factorial(int numero) {
    if (numero == 1) {
        return 1;
    }

    return numero * factorial(numero - 1);
}
```

Si llamamos a `factorial(3)`, las llamadas se van produciendo hasta alcanzar la condición base:

```
factorial(3)
    → factorial(2)
        → factorial(1)
```

Cuando se alcanza `factorial(1)`, las llamadas comienzan a **terminar en sentido inverso**, devolviendo sus resultados.

La condición base es fundamental. Si una función recursiva nunca alcanza una condición que detenga las llamadas, continuará llamándose hasta producir un error por agotamiento de la pila de llamadas (`StackOverflowError`).

Cada llamada recursiva tiene su propio conjunto de parámetros y variables locales. Java mantiene estas llamadas en la **pila de ejecución (stack)** hasta que cada una termina.

La recursividad puede resolver determinados problemas de forma elegante, especialmente aquellos que tienen una estructura naturalmente repetitiva o jerárquica. Sin embargo, no siempre es la mejor opción: una solución iterativa mediante bucles puede consumir menos memoria y resultar más sencilla.

> la recursividad consiste en que un método se llame a sí mismo para resolver versiones cada vez más pequeñas del problema. Necesita una **condición base** que detenga las llamadas y un **caso recursivo** que continúe el proceso.