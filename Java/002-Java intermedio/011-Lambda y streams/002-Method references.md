### Method references

Los **method references** son una forma todavía más compacta de escribir una expresión lambda cuando **el comportamiento de la lambda ya existe en un método**.

En lugar de escribir una lambda que simplemente llama a un método existente, podemos hacer referencia directamente a ese método.

Por ejemplo, si tenemos:

```java
lista.forEach(nombre -> System.out.println(nombre));
```

podemos escribir:

```java
lista.forEach(System.out::println);
```

`::` es el operador utilizado para crear una referencia a un método.

La idea fundamental es:

```
Lambda
→ describe una operación

Method reference
→ señala directamente a un método que ya realiza esa operación
```

Por eso un method reference **no crea un nuevo comportamiento**. Simplemente proporciona una referencia a un método existente que puede utilizarse donde Java espera una **interfaz funcional**.

Existen diferentes formas de referencias, dependiendo de dónde se encuentre el método:

```java
Clase::método
objeto::método
Clase::new
```

La última forma permite hacer referencia a un **constructor**.

Por ejemplo:

```java
Persona::new
```

Una condición importante es que la firma del método referenciado sea compatible con el **único método abstracto de la interfaz funcional** que se espera.

Por eso una referencia como:

```java
System.out::println
```

puede utilizarse en un contexto donde Java espera una operación compatible con `Consumer`.

### Lambda vs method reference

```java
Lambda:
nombre -> System.out.println(nombre)

Method reference:
System.out::println
```

Ambas expresan esencialmente el mismo comportamiento, pero el method reference resulta más **directo y legible** cuando el método ya existe.

>un method reference permite **referenciar directamente un método o constructor existente** mediante `::`, evitando escribir una lambda cuando esta únicamente llama a ese método.