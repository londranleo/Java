# Tipos primitivos

Los tipos primitivos son los tipos de datos más básicos y simples que tiene Java para guardar información, como números o valores de verdadero/falso.

Java tiene 8 tipos primitivos en total, y cada uno sirve para guardar un tipo de información.

### Enteros

| Tipo  |  Bits   |                     Rango                      | Valor por defecto |
| ----- | :-----: | :--------------------------------------------: | :---------------: |
| byte  | 8 bits  |                 -128 hasta127                  |         0         |
| short | 16 bits |               -32768 hasta 32767               |         0         |
| int   | 32 bits |       -2.147.483.648 hasta 2.147.483.648       |         0         |
| long  | 64 bits | -9223372036854775808 hasta 9223372036854775807 |         0         |
|       |         |                                                |                   |
### Decimales

| Tipo   |  Bits   |            Rango             | Valor por defecto |
| ------ | :-----: | :--------------------------: | :---------------: |
| float  | 32 bits | -3.4 × 10³⁸ hasta 3.4 × 10³⁸ |        0.0        |
| double | 64 bits | -1.79E+308 hasta +1.79E+308  |        0.0        |
### Otros

| Tipo    |  Bits   |    Rango     | Valor por defecto |
| ------- | :-----: | :----------: | :---------------: |
| Char    | 16 bits |   Unicode    |     0 o nulo      |
| boolean | 64 bits | false o true |       false       |

## byte

`byte` es un tipo de dato primitivo de Java que se usa para almacenar números enteros (sin decimales). Es el tipo entero más pequeño: ocupa solo 8 bits de memoria, por lo que su rango de valores es muy limitado, desde -128 hasta 127.

Si no se le asigna ningún valor, su valor por defecto es 0.

```java
byte cantidad = 100;
```

## short

`short` es un tipo de dato primitivo de Java que se usa para almacenar números enteros (sin decimales). Ocupa 16 bits de memoria, por lo que puede representar valores dentro de un rango limitado: desde -32768 hasta 32767.

Si no se le asigna ningún valor, su valor por defecto es 0.

```java
short edad = 25;
```
## int

`int` es uno de los tipos de datos primitivos de Java, utilizado para almacenar **números enteros** (sin decimales), tanto positivos como negativos.

Ocupa **4 bytes (32 bits)** de memoria, lo que le permite representar valores entre **-2.147.483.648** y **2.147.483.647**. Si necesitas un número fuera de ese rango, debes usar `long` en su lugar.

Para declarar una variable de tipo `int`, se escribe el tipo seguido del nombre de la variable y, opcionalmente, un valor inicial:

```java
int edad = 25;
int temperatura = -10;
int contador;
```

Si no se le asigna un valor al declararla, `int` toma por defecto el valor `0` cuando se trata de un atributo de una clase. En el caso de variables locales (declaradas dentro de un método), Java obliga a asignarles un valor antes de poder utilizarlas.

## long

`long` es un tipo de dato primitivo de Java que se usa para almacenar números enteros (sin decimales). Ocupa 64 bits de memoria, lo que le permite representar un rango de valores mucho más amplio que otros tipos enteros: desde aproximadamente -9223372036854775808 hasta 9223372036854775807.

Si no se le asigna ningún valor, su valor por defecto es 0.

Al escribir un valor literal de tipo `long` en el código, es necesario añadir la letra `L` al final, para indicar que ese número debe tratarse como `long` y no como un tipo entero más pequeño.

```java
long poblacion = 8000000000L;
```

## float

`float` es un tipo de dato primitivo de Java que se usa para almacenar números con decimales (números de punto flotante). Ocupa 32 bits de memoria y ofrece una precisión limitada, suficiente para la mayoría de los casos donde no se requiere una exactitud extrema.

Si no se le asigna ningún valor, su valor por defecto es 0.0.

Al escribir un valor literal de tipo `float` en el código, es necesario añadir la letra `f` al final, para indicar que ese número debe tratarse como `float`.

```java
float altura = 1.75f;
```
## double

`double` es un tipo de dato primitivo de Java que se usa para almacenar números con decimales (números de punto flotante). Ocupa 64 bits de memoria, lo que le da mayor precisión que `float`, por lo que es el tipo con decimales más utilizado por defecto en Java.

Si no se le asigna ningún valor, su valor por defecto es 0.0.

A diferencia de `float`, no es necesario añadir ninguna letra especial al escribir un valor literal de tipo `double`, ya que es el tipo decimal que Java asume por defecto.

```java
double peso = 68.5;
```

## char

`char` es un tipo de dato primitivo de Java que se usa para almacenar un único carácter,  Ocupa 16 bits de memoria y, internamente, cada carácter se representa como un número (su valor en la codificación Unicode), aunque a la hora de trabajar con él se ve y se usa como un carácter.

Su valor se escribe entre comillas simples.

Si no se le asigna ningún valor, su valor por defecto es el carácter nulo (equivalente al número 0), que no es visible.

```java
char letra = 'A';
```
## boolean

`boolean` es un tipo de dato primitivo de Java que se usa para representar un valor de verdad: solo puede ser `true` (verdadero) o `false` (falso). No admite ningún otro valor.

Si no se le asigna ningún valor, su valor por defecto es `false`.

```java
boolean activo = true;
```

>[!Cuidado]
>A diferencia de otros lenguajes, en Java un `boolean` no puede
>tratarse como un número (no equivale a 0 o 1), por lo que no admite
>operaciones numéricas ni conversiones automáticas con tipos enteros.
