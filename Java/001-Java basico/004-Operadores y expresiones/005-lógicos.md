## Operadores lógicos

Los **operadores lógicos** permiten combinar, invertir o evaluar varias condiciones booleanas. Se utilizan cuando una decisión depende de **más de una condición**.

Trabajan principalmente con valores `boolean` y producen como resultado otro `boolean`: `true` o `false`.

Los principales operadores son:

| Operador | Significado    |
| -------- | -------------- |
| `&&`     | AND — y        |
| `\|\|`   | OR — o         |
| `!`      | NOT — negación |

### `&&` — AND

El operador `&&` devuelve `true` **solo cuando todas las condiciones que combina son verdaderas**.

```java
edad >= 18 && tieneEntrada
```

Para que el resultado sea `true`, tanto `edad >= 18` como `tieneEntrada` deben ser `true`.

Si cualquiera de las condiciones es `false`, el resultado será `false`.

### `||` — OR

El operador `||` devuelve `true` cuando **al menos una de las condiciones es verdadera**.

```java
esAdmin || esModerador
```

El resultado será `true` si `esAdmin` es `true`, si `esModerador` es `true` o si ambas son verdaderas. Solo será `false` cuando **todas** las condiciones sean falsas.

### `!` — NOT

El operador `!` **invierte el valor booleano** de una expresión.

```java
!activo
```

Si `activo` es `true`, `!activo` será `false`, y viceversa.

A diferencia de `&&` y `||`, `!` es un operador **unario**, porque trabaja sobre un único operando.

### Evaluación de cortocircuito

`&&` y `||` utilizan **evaluación de cortocircuito**.

Esto significa que Java puede dejar de evaluar una expresión cuando ya conoce cuál será el resultado final.

Con `&&`, si la primera condición es `false`, no es necesario evaluar las siguientes, porque el resultado completo ya tendrá que ser `false`.

Con `||`, si la primera condición es `true`, Java tampoco necesita evaluar las siguientes, porque el resultado ya será `true`.

Esto no solo puede mejorar la eficiencia, sino que también permite escribir condiciones en las que una segunda expresión solo se evalúe cuando sea necesario.