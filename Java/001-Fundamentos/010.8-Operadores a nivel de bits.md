## Operadores a nivel de bits

Los **operadores a nivel de bits** permiten trabajar directamente con los bits que forman la representación binaria de un valor entero. En lugar de operar sobre el número como un valor completo, Java realiza la operación **bit por bit**.

Se utilizan principalmente con tipos enteros como `byte`, `short`, `int` y `long`.

Los principales operadores son:

|Operador|Función|
|---|---|
|`&`|AND bit a bit|
|`|`|
|`^`|XOR bit a bit|
|`~`|NOT bit a bit|
|`<<`|Desplazamiento a la izquierda|
|`>>`|Desplazamiento a la derecha con signo|
|`>>>`|Desplazamiento a la derecha sin signo|

### `&` — AND

Compara cada bit de los dos operandos. Un bit del resultado será `1` **solo cuando ambos bits sean `1`**.

### `|` — OR

Compara cada bit de los operandos. El resultado tendrá `1` cuando **al menos uno de los dos bits sea `1`**.

### `^` — XOR

El resultado tendrá `1` cuando los dos bits sean **diferentes**. Si ambos son iguales, el resultado será `0`.

### `~` — NOT

Es un operador unario que **invierte cada bit** del operando: los `1` pasan a `0` y los `0` pasan a `1`.

### Desplazamientos

Los operadores `<<`, `>>` y `>>>` desplazan los bits de un número hacia la izquierda o hacia la derecha.

`<<` desplaza hacia la izquierda y añade ceros por la derecha.

`>>` desplaza hacia la derecha conservando el **bit de signo**, por lo que está relacionado con la representación de números negativos.

`>>>` también desplaza hacia la derecha, pero introduce **ceros por la izquierda**, independientemente del signo.

Los desplazamientos son operaciones especialmente útiles cuando se trabaja con **representaciones binarias, máscaras de bits, flags, protocolos o estructuras de datos de bajo nivel**.

Es importante no confundir estos operadores con `&&` y `||`. Aunque sus símbolos son parecidos, `&` y `|` realizan operaciones **bit a bit**, mientras que `&&` y `||` trabajan con expresiones booleanas y utilizan evaluación de cortocircuito.

>Los operadores a nivel de bits permiten manipular directamente la representación binaria de valores enteros. Los operadores `&`, `|`, `^` y `~` realizan operaciones sobre bits, mientras que `<<`, `>>` y `>>>` desplazan esos bits.