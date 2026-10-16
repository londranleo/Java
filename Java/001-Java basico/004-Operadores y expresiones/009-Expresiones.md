## Expresiones

Una **expresión** es una combinación de **valores, variables, operadores y llamadas a métodos** que Java puede evaluar para producir un **resultado**.

Por ejemplo:

```java
int resultado = 10 + 5;
```

`10 + 5` es una expresión porque Java la evalúa y obtiene `15`.

Una expresión no tiene por qué ser únicamente una operación matemática:

```java
edad > 18
```

produce un valor `boolean` (`true` o `false`).

También puede contener variables:

```java
a + b
```

o llamadas a métodos:

```java
Math.max(10, 20)
```

### Tipos de expresiones

Dependiendo de lo que hagan, podemos encontrar expresiones que producen distintos tipos de resultados:

```java
10 + 5          → int
precio * 2      → número
edad >= 18      → boolean
nombre + "!"    → String
```

Los **operadores** determinan cómo se combinan los elementos de una expresión.

Por ejemplo:

```java
a + b * 2
```

Java no evalúa necesariamente las operaciones de izquierda a derecha. Los operadores tienen una **precedencia**, que determina qué operaciones se realizan primero.

También podemos utilizar paréntesis para indicar explícitamente el orden:

```java
(a + b) * 2
```

### Expresión vs instrucción

Una **expresión** produce un valor.

Una **instrucción (statement)** es una unidad de código que Java puede ejecutar.

Por ejemplo:

```java
10 + 5
```

es una expresión.

```java
int resultado = 10 + 5;
```

es una instrucción de declaración y asignación que contiene una expresión.

>una expresión es una combinación de elementos que Java **evalúa para obtener un resultado**. Puede producir valores numéricos, booleanos, cadenas, objetos, etc., y los operadores y sus reglas de precedencia determinan cómo se obtiene ese resultado.