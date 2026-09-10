# ¿Qué es una variable?

Una **variable** es un espacio de memoria identificado mediante un nombre que permite **almacenar un valor durante la ejecución de un programa**.

El valor almacenado puede cambiar a lo largo de la ejecución, de ahí el nombre de variable.

En Java, una variable siempre está asociada a un **tipo de dato**, que determina qué clase de valor puede almacenar y qué operaciones se pueden realizar con él.

```java
int edad = 25;
```

En este caso:

- `int` indica el **tipo de dato** de la variable.
    
- `edad` es el **nombre** de la variable.
    
- `25` es el **valor** almacenado.
    
- `=` asigna el valor a la variable.
    

Una variable puede cambiar su valor después de haber sido creada:

```java
int edad = 25;

edad = 26;
```

Después de la segunda asignación, `edad` contiene `26`.

El tipo de una variable no cambia durante su existencia. Si una variable se declara como `int`, solamente puede almacenar valores compatibles con `int`.

```java
int edad = 25;
```

No se puede asignar directamente un valor de otro tipo incompatible:

```java
int edad = "25"; // Error
```

Una variable se utiliza para que el programa pueda **trabajar con datos que necesita conservar temporalmente**, consultar, modificar y utilizar posteriormente en operaciones o instrucciones.



