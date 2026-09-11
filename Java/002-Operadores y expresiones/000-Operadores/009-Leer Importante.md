# Precedencia

La precedencia de operadores determina **en qué orden se evalúan las operaciones** cuando una misma expresión combina varios operadores. Al igual que en matemáticas, donde la multiplicación se resuelve antes que la suma, Java sigue unas reglas fijas para decidir qué operación se calcula primero.

```java
int resultado = 5 + 3 * 2; // 11, no 16
```

Aquí, aunque la suma aparece antes en la expresión, la multiplicación tiene mayor precedencia, así que se calcula primero (`3 * 2 = 6`) y después se suma (`5 + 6 = 11`).

## Orden general (de mayor a menor precedencia)

De forma simplificada, este es el orden en el que Java evalúa los operadores más comunes:

1. Paréntesis `()`
2. Incremento/decremento `++` `--`
3. Multiplicación, división, resto `*` `/` `%`
4. Suma y resta `+` `-`
5. Comparación `<` `>` `<=` `>=`
6. Igualdad `==` `!=`
7. AND lógico `&&`
8. OR lógico `||`
9. Asignación `=`

Los operadores con mayor precedencia se calculan antes que los de menor precedencia, sin importar el orden en el que aparezcan escritos en la expresión.

## Uso de paréntesis

Los paréntesis tienen la precedencia más alta de todas, por lo que se pueden usar para forzar el orden de evaluación que se necesite, independientemente de las reglas por defecto:

```java
int resultado = (5 + 3) * 2; // 16
```

Aquí, gracias a los paréntesis, la suma se calcula primero (`5 + 3 = 8`) y después se multiplica (`8 * 2 = 16`).

Aunque memorizar todas las reglas de precedencia es posible, en la práctica es muy recomendable usar paréntesis siempre que una expresión combine varios operadores, ya que hace el código más claro y evita errores por confundir el orden de evaluación.