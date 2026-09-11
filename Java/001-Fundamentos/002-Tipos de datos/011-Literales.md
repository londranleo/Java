# Literales

Un **literal** es un valor fijo escrito directamente en el código fuente, tal y como se representa a simple vista, sin necesidad de calcularlo ni obtenerlo de ninguna otra parte. Es la forma en que se escribe un dato concreto para asignarlo a una variable o usarlo directamente en una expresión.

```java
int edad = 25;
```

Aquí, `25` es un literal: el valor exacto que se está escribiendo en el código.

Existen distintos tipos de literales según el tipo de dato que representan: numéricos (enteros y decimales), de carácter, de texto y booleanos. Cada uno se escribe de una forma concreta para que Java sepa interpretarlo correctamente (por ejemplo, un carácter entre comillas simples o un texto entre comillas dobles).

Los literales numéricos enteros pueden escribirse además en distintos sistemas de numeración:

```java
int decimal = 10;
int binario = 0b1010;
int octal   = 012;
int hexadecimal = 0xA;
```

Todos representan el mismo valor, solo cambia la forma en que se escribe.

También es posible usar guiones bajos (`_`) dentro de un literal numérico para facilitar su lectura, sin que afecten al valor real:

```java
int poblacion = 8_000_000;
```