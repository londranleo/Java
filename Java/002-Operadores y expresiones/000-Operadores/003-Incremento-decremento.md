# Incremento/decremento

Java ofrece dos operadores especiales para aumentar o disminuir en 1 el valor de una variable numérica, sin tener que escribir la operación completa: `++` para incrementar y `--` para decrementar.

En lugar de escribir:

```java
edad = edad + 1;
```

se puede escribir simplemente:

```java
edad++;
```

Y de forma equivalente, para restar 1:

```java
edad--;
```

## Prefijo y sufijo

Estos operadores se pueden colocar antes (`++edad`) o después (`edad++`) de la variable, y aunque en ambos casos el resultado final sobre la variable es el mismo, la diferencia importa cuando el incremento se usa **dentro de una expresión**, es decir, al mismo tiempo que se usa el valor de la variable para otra cosa (como asignarlo o mostrarlo).

- **Postincremento (`edad++`)**: primero se usa el valor actual de la variable, y después se incrementa.
- **Preincremento (`++edad`)**: primero se incrementa la variable, y después se usa ese nuevo valor.

```java
int edad = 20;
int a = edad++; // a vale 20, y edad pasa a valer 21
```

```java
int edad = 20;
int b = ++edad; // edad pasa a valer 21, y b vale 21
```

Lo mismo aplica al decremento, con `edad--` y `--edad`, pero restando 1 en lugar de sumarlo.

Cuando el incremento o decremento se usa en una línea propia, sin combinarlo con otra operación, no hay diferencia entre usar la forma prefijo o sufijo, ya que el resultado final sobre la variable es idéntico.