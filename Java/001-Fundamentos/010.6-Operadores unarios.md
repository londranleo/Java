## Operadores unarios

Los **operadores unarios** son aquellos que trabajan sobre **un único operando**. A diferencia de los operadores binarios, que necesitan dos operandos, los unarios modifican, invierten o determinan información sobre un solo valor.

Los principales operadores unarios son:

|Operador|Función|
|---|---|
|`+`|Indica un valor positivo|
|`-`|Cambia el signo del valor|
|`!`|Invierte un `boolean`|
|`++`|Incrementa en 1|
|`--`|Decrementa en 1|

El operador `+` unario simplemente indica que el valor es positivo y normalmente no produce ningún cambio apreciable en el valor.

El operador `-` cambia el signo del operando:

```java
int numero = 10;
int resultado = -numero; // -10
```

El operador `!` trabaja con valores `boolean` e invierte su resultado. Si el valor es `true`, pasa a ser `false`, y viceversa.

Los operadores `++` y `--` aumentan o disminuyen una variable numérica en una unidad. Pueden colocarse **antes o después** de la variable:

```java
int numero = 5;

++numero; // 6
numero--; // 5
```

La posición es importante cuando el operador forma parte de una expresión. Si aparece **antes** (`++numero`), primero se realiza el incremento y después se utiliza el valor. Si aparece **después** (`numero++`), primero se utiliza el valor actual y posteriormente se realiza el incremento.

Los operadores unarios no todos tienen el mismo comportamiento: algunos producen un nuevo valor a partir del operando, mientras que `++` y `--` modifican el valor de una variable.