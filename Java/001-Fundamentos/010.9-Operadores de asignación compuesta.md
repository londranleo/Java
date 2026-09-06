## Operadores de asignación compuesta

Los **operadores de asignación compuesta** combinan una operación con una asignación. Permiten utilizar el valor actual de una variable, realizar una operación sobre él y guardar nuevamente el resultado en la misma variable.

Los principales son:

| Operador | Equivalencia      |
| -------- | ----------------- |
| `+=`     | `a = a + valor`   |
| `-=`     | `a = a - valor`   |
| `*=`     | `a = a * valor`   |
| `/=`     | `a = a / valor`   |
| `%=`     | `a = a % valor`   |
| `&=`     | `a = a & valor`   |
| `        | =`                |
| `^=`     | `a = a ^ valor`   |
| `<<=`    | `a = a << valor`  |
| `>>=`    | `a = a >> valor`  |
| `>>>=`   | `a = a >>> valor` |

Por ejemplo:

```java
int puntos = 10;
puntos += 5;
```

Es equivalente a:

```java
puntos = puntos + 5;
```

Después de la operación, `puntos` contiene `15`.

La ventaja principal de estos operadores es que **simplifican expresiones en las que se utiliza la propia variable como parte de la operación**.

También hay que tener en cuenta que las asignaciones compuestas pueden implicar conversiones de tipo que no ocurren de la misma forma con una asignación normal. Por ejemplo:

```java
byte numero = 10;
numero += 5;
```

Esta operación es válida porque una asignación compuesta incorpora implícitamente la conversión necesaria.

>Los operadores de asignación compuesta combinan una operación y una asignación en una sola expresión. Permiten actualizar el valor de una variable de forma más compacta y legible