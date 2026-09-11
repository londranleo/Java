# Conversión automática

Cuando una expresión combina operandos de **distintos tipos numéricos**, Java convierte automáticamente uno de ellos para que ambos queden del mismo tipo antes de realizar la operación. A esto se le llama **conversión implícita** (o *widening*), y ocurre sin que el programador tenga que escribir nada especial.

```java
int a = 5;
double b = 2.0;

double resultado = a + b; // a se convierte automáticamente a double: 7.0
```

Aquí, `a` (que es `int`) se convierte temporalmente a `double` para poder sumarse con `b`, y el resultado final también es `double`.

## Regla general

Java siempre convierte hacia el tipo **más amplio** (el que puede representar más valores o con más precisión), nunca al revés, para evitar perder información. El orden de amplitud, de menor a mayor, es aproximadamente:

```text
byte → short → int → long → float → double
```

Si en una expresión se mezclan tipos distintos, el resultado adopta el tipo más amplio de los que participan. Por ejemplo, `int` combinado con `double` da como resultado `double`; `int` combinado con `long` da como resultado `long`.

## char en expresiones numéricas

Los valores `char` también pueden participar en expresiones numéricas, ya que internamente Java los representa como números (su valor Unicode). Al combinarlos con un tipo numérico, se convierten automáticamente a `int`:

```java
char letra = 'A';
int codigo = letra + 1; // 'A' se convierte a su valor numérico (65), resultado: 66
```

## Cuando la conversión automática no es suficiente

La conversión automática solo ocurre hacia tipos más amplios. Si se quiere ir en sentido contrario (por ejemplo, de `double` a `int`), Java no lo hace de forma automática porque implicaría perder información (como los decimales), y es necesario forzarlo de forma explícita mediante un *casting*, algo que corresponde a otro tema.