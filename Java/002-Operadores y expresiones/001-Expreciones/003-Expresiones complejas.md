# Expresiones complejas

Una **expresión compleja** es una expresión que combina varios operadores y operandos en una misma línea, en lugar de realizar una única operación simple. Java las evalúa aplicando las reglas de **precedencia** (qué operador se calcula antes) y **asociatividad** (en qué orden se resuelven operadores del mismo nivel) ya vistas anteriormente.

```java
int resultado = 5 + 3 * 2 - 4 / 2;
```

Aquí Java resuelve primero las multiplicaciones y divisiones (`3 * 2 = 6` y `4 / 2 = 2`), y después las sumas y restas de izquierda a derecha (`5 + 6 - 2 = 9`).

## Combinando distintos tipos de operadores

Una expresión compleja no tiene por qué limitarse a operadores aritméticos: también puede mezclar comparaciones y operadores lógicos en una misma línea.

```java
boolean resultado = (edad >= 18) && (edad < 65);
```

Aquí primero se resuelven las comparaciones dentro de los paréntesis, y después se combina el resultado con `&&`.

## El papel de los paréntesis

Cuando una expresión combina muchos operadores, seguir mentalmente el orden de precedencia puede volverse complicado y propenso a errores. Por eso, en expresiones complejas es muy recomendable usar paréntesis para dejar claro qué se quiere calcular primero, aunque no sean estrictamente necesarios según las reglas de precedencia:

```java
int resultado = 5 + (3 * 2) - (4 / 2); // mismo resultado, pero más claro
```

## Legibilidad

Cuanto más compleja es una expresión, más importante es que sea fácil de leer. Dividir una expresión muy larga en varias variables intermedias, aunque técnicamente no sea necesario, suele hacer el código más claro y más fácil de depurar:

```java
int producto = 3 * 2;
int division = 4 / 2;
int resultado = 5 + producto - division;
```

Esto no cambia el resultado final, pero facilita entender qué representa cada parte de la expresión.