# Asociatividad

La asociatividad determina **en qué orden se evalúan las operaciones cuando varios operadores tienen la misma precedencia** dentro de una misma expresión. Mientras que la precedencia decide qué operador se resuelve antes entre operadores distintos, la asociatividad decide el orden cuando el operador es el mismo (o tiene el mismo nivel).

## Asociatividad de izquierda a derecha

La mayoría de los operadores aritméticos (`+`, `-`, `*`, `/`, `%`) se evalúan de **izquierda a derecha** cuando aparecen varios seguidos con la misma precedencia:

```java
int resultado = 10 - 3 - 2;
```

Aquí, al tener `-` la misma precedencia consigo mismo, se evalúa de izquierda a derecha: primero `10 - 3 = 7`, y después `7 - 2 = 5`. Si la asociatividad fuera de derecha a izquierda, el resultado sería distinto (`10 - (3 - 2) = 9`).

Esto también aplica a operadores de comparación y lógicos cuando se combinan varios del mismo tipo:

```java
boolean resultado = true && false && true; // se evalúa de izquierda a derecha
```

## Asociatividad de derecha a izquierda

El operador de asignación `=` funciona al revés: se evalúa de **derecha a izquierda**. Esto permite encadenar asignaciones en una misma línea:

```java
int a, b, c;
a = b = c = 5;
```

Aquí, primero se asigna `c = 5`, después `b = c` (que vale 5), y finalmente `a = b` (que también vale 5). Todas las variables terminan valiendo 5, gracias a que la asignación se resuelve de derecha a izquierda.

## Por qué importa

Cuando una expresión combina operadores con la misma precedencia, el orden de evaluación afecta directamente al resultado final, especialmente con operaciones donde el orden importa, como la resta o la división. Conocer la asociatividad evita confusiones al interpretar o escribir expresiones que combinan varios operadores del mismo nivel.