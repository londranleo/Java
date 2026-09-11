# Expresiones

Una **expresión** es cualquier combinación de valores, variables y operadores que Java puede evaluar para producir un único resultado. Puede ser tan simple como un número suelto o tan compleja como una combinación de varias operaciones.

```java
int resultado = 5 + 3 * 2;
```

Aquí, `5 + 3 * 2` es una expresión: Java la evalúa y produce un valor (`11`), que después se guarda en la variable `resultado`.

## Operandos

Los **operandos** son los valores sobre los que actúa una operación. Pueden ser literales (valores escritos directamente, como `5`), variables, o incluso el resultado de otra expresión.

```java
int a = 5;
int b = 3;
int suma = a + b; // a y b son los operandos
```

## Operadores

Los **operadores** son los símbolos que indican qué operación se realiza sobre los operandos. Java tiene varios tipos, según lo que hacen:

- **Aritméticos**: `+`, `-`, `*`, `/`, `%` (realizan cálculos matemáticos).
- **De comparación**: `==`, `!=`, `>`, `<`, `>=`, `<=` (comparan valores y devuelven `true` o `false`).
- **Lógicos**: `&&`, `||`, `!` (combinan condiciones booleanas).
- **De asignación**: `=`, `+=`, `-=`, etc. (asignan un valor a una variable).

Cada operador necesita uno o dos operandos para funcionar. Por ejemplo, `+` necesita dos operandos (`a + b`), mientras que `!` (negación lógica) solo necesita uno (`!true`).

## Evaluación

**Evaluar** una expresión significa calcular su resultado final, aplicando los operadores sobre los operandos en el orden que corresponda. Java evalúa cada expresión de forma automática siguiendo sus propias reglas internas (como la precedencia entre operadores), sin que el programador tenga que indicar el orden paso a paso.

```java
int resultado = (2 + 3) * 4; // Java evalúa primero (2 + 3), y después multiplica por 4
```

Toda expresión, por sencilla o compleja que sea, termina produciendo un único valor, que puede usarse directamente (por ejemplo, dentro de un `System.out.println`) o guardarse en una variable para usarlo más adelante.