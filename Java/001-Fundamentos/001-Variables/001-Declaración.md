# Declaración

Declarar una variable significa indicarle a Java que vas a utilizar un espacio en la memoria del ordenador para guardar un dato, y decirle qué tipo de dato va a guardar y con qué nombre lo vas a identificar.

Cuando declaras una variable, no le estás dando todavía un valor. Solo le estás diciendo al programa: "voy a necesitar un espacio para guardar un número (o un texto, o un valor verdadero/falso, etc.), y quiero llamarlo de esta forma".

En Java, para declarar una variable se escribe primero el **tipo de dato** que va a contener, y después el **nombre** que le das:

```java
int edad;
```

Aquí `int` indica el tipo de dato (un número entero) y `edad` es el nombre que le has puesto a la variable.

A partir de este momento, Java reserva un espacio en memoria para ese dato y ya puedes referirte a él usando el nombre `edad` en el resto del código.

Es importante saber que en Java, a diferencia de otros lenguajes, siempre debes indicar el tipo de dato al declarar una variable. Esto se debe a que Java es un lenguaje donde el tipo de cada dato debe quedar definido de forma clara y fija.

También puedes declarar varias variables del mismo tipo en una sola línea, separándolas por comas:

```java
int edad, altura, peso;
```

Una variable declarada, pero sin haberle asignado todavía un valor, no puede utilizarse en operaciones ni mostrarse en pantalla. Java no permite trabajar con una variable que aún no tiene ningún dato guardado.