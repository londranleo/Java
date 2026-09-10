# Inicialización

Inicializar una variable significa darle un valor por primera vez después de haberla declarado. Es el momento en el que esa "caja" de memoria, que hasta entonces estaba vacía, pasa a contener realmente un dato.

En Java, la inicialización se hace utilizando el signo `=`, seguido del valor que quieres guardar:

```java
int edad = 25;
```

En este ejemplo, la variable `edad` no solo se ha declarado (indicando que es de tipo `int`), sino que también se ha inicializado con el valor `25` en la misma línea.

También es posible declarar una variable primero y darle un valor más adelante, en una línea distinta:

```java
int edad;
edad = 25;
```

En este caso, la variable se declara sin valor, y la inicialización ocurre después, cuando se le asigna `25`.

Es importante inicializar una variable antes de utilizarla. Si intentas usar una variable que ha sido declarada pero nunca inicializada, Java no te dejará compilar el programa, porque no sabe qué valor tiene todavía.

Una variable puede inicializarse con un valor fijo escrito directamente en el código, como en los ejemplos anteriores, o con el resultado de una operación o expresión, siempre que ese resultado sea del mismo tipo que la variable:

```java
int suma = 10 + 5;
```