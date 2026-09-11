# Comparación

Los operadores de comparación permiten comparar dos valores entre sí, y el resultado de esa comparación siempre es un valor **booleano**: `true` (verdadero) o `false` (falso). Se usan constantemente para tomar decisiones dentro de un programa, por ejemplo en condiciones `if` o bucles.

Los operadores de comparación en Java son:

| Operador | Significado |
|----------|-------------|
| `==` | igual a |
| `!=` | distinto de |
| `>` | mayor que |
| `<` | menor que |
| `>=` | mayor o igual que |
| `<=` | menor o igual que |

```java
int a = 5;
int b = 8;

boolean resultado = a < b; // true
```

## Comparar números y caracteres

Con tipos primitivos (`int`, `double`, `char`, etc.) estos operadores comparan directamente el valor, tal y como cabría esperar:

```java
System.out.println(5 == 5);  // true
System.out.println(5 != 5);  // false
System.out.println(7 > 3);   // true
```

## El problema de comparar texto con ==

Con objetos, como los `String`, el operador `==` **no compara el contenido del texto**, sino si ambas variables apuntan exactamente al mismo objeto en memoria. Esto puede dar resultados inesperados:

```java
String nombre1 = new String("Ana");
String nombre2 = new String("Ana");

System.out.println(nombre1 == nombre2); // false, aunque el texto sea igual
```

Para comparar si el **contenido** de dos textos es igual, hay que usar el método `equals()`:

```java
System.out.println(nombre1.equals(nombre2)); // true
```

Esta diferencia es importante porque es un error muy común usar `==` para comparar cadenas de texto esperando que compare su contenido, cuando en realidad está comparando si son el mismo objeto.