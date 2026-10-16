## Tipos Primitivos

Java mantiene 8 tipos de tipos de datos básicos que **no** son objetos. Son valores puros que se almacenas directamente en la memoria _Stack_ (pila), lo que los hace extremadamente rápidos de procesar.  

Se divide en 4 grupos: Enteros, Flotantes, Caracteres y Booleanos.

### Números enteros (Integer types)

sirve para contar cosas que no tienen decimales hay 4 tipos, dependiendo de lo grande que sea el numero que quieres guardar. 

| Tipo  | Tammano | Rango                            |
| ----- | ------- | -------------------------------- |
| byte  | 8 bits  | -128 a 127                       |
| short | 16 bits | -32,768 a 32,767                 |
| int   | 32 bits | -2 mil millones a 2 mil millones |
| long  | 64 bits | Gigantesco (9 trillones...)      |

> Si quieres usar `long`, debes poner una "L" al final del numero, porque si no, Java intentara tratarlo como un `int` y si es muy grande, dara error.

```java
byte tipoByte = 127;
short tipoShort = 32000;
int habitaciones = 12345678;
long distanciaEstrella = 9460730472580800L
```


---
### Números decimales (Floating point types)

Para cada numero con partes fraccionaria se utiliza el estándar **IEEE 754** .

| TIPO   | TAMANO  | PRECISION       |
| ------ | ------- | --------------- |
| float  | 32 bits | 6-7 decimales   |
| double | 64 bits | 15-16 decimales |

Al igual que con los enteros, hay un estándar que es `double`. Java trata cualquier decimal (`3.14`) como un` double` por defecto. Si quieres forzar un `float`, debes usar la `f`.

```java
double pi = 3.1415926535;
float gravedad = 9.8f; 
```

---
### Carácter (Char)

El tipo `char` se usa para almacenar **un solo carácter**. En Java un `char` ocupa **2 bytes (16bits)** por que Java usa **Unicode** (UTF-16) internamente. Este permite guardar caracteres chinos, emojis, etc.

Define siempre con **comillas simples** `' '`

```java
char letra = 'A';
char simbolo = '@';
char unicode = '\u0041' // es la letra 'A' em codigo Unicode
```

> [!Cuidado] 
> Cuidado `'A'` (char) no es lo mismo que `"A"` (String). Las comillas dobles una cadena de caracteres, que es un Objeto, no un primitivo.

---
### Booleanos (boolean)

El tipo mas simple. Solo tiene dos valores posibles `true` (verdadero) o `false` (falso).


```java
boolean esJavaDivertido = true;
boolean meGusraPHP = false
```

## Tipos Referencia (object)

 Una variable de tipo referencia almacena la referencia a un objeto en memoria, permitiendo acceder a sus datos y métodos.

```java
String nombre = null; //valor por default 
nombre "juan";
```


# [[003-Reglas para los nombre variables]]





