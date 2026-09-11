# Expresiones booleanas

Una **expresión booleana** es una expresión cuyo resultado siempre es un valor de tipo `boolean`: `true` o `false`. Se usan constantemente para tomar decisiones dentro de un programa, ya que son la base de estructuras como `if` o los bucles.

```java
boolean esMayor = 10 > 5; // true
```

## Cómo se forman

Una expresión booleana puede construirse de varias formas:

- Usando directamente los valores `true` o `false`.
- Usando **operadores de comparación** (`==`, `!=`, `>`, `<`, `>=`, `<=`), que comparan dos valores y devuelven un resultado booleano.
- Usando **operadores lógicos** (`&&`, `||`, `!`), que combinan o invierten valores booleanos.

```java
int edad = 20;
boolean tieneEdad = edad >= 18;       // comparación
boolean puedeEntrar = tieneEdad && true; // combinación lógica
```

## Operadores lógicos

- `&&` (AND): el resultado es `true` solo si ambas condiciones son `true`.
- `||` (OR): el resultado es `true` si al menos una de las condiciones es `true`.
- `!` (NOT): invierte el valor booleano (`true` pasa a `false`, y viceversa).

```java
boolean resultado = (5 > 3) && (2 < 4); // true, porque ambas condiciones son verdaderas
boolean resultado2 = !(5 > 3);          // false, porque invierte un resultado verdadero
```

## Evaluación cortocircuitada

Los operadores `&&` y `||` tienen un comportamiento especial llamado **evaluación cortocircuitada**: si el resultado ya puede determinarse con la primera condición, Java no evalúa la segunda.

- Con `&&`, si la primera condición es `false`, el resultado ya es `false`, así que la segunda condición ni se comprueba.
- Con `||`, si la primera condición es `true`, el resultado ya es `true`, así que la segunda condición ni se comprueba.

Esto no solo ahorra procesamiento, sino que también evita errores en casos donde la segunda condición dependería de que la primera se cumpla.