## `continue`

`continue` se utiliza dentro de un bucle para **saltar el resto del código de la vuelta actual** y pasar directamente a la siguiente iteración.

A diferencia de `break`, **no termina el bucle**.

```java
for (int i = 0; i < 5; i++) {
    if (i == 2) {
        continue;
    }

    System.out.println(i);
}
```

Cuando `i` vale `2`, se ejecuta `continue`. Java deja de ejecutar el resto del bloque en esa vuelta y pasa a la siguiente.

La diferencia fundamental es:

```java
break     → termina el bucle
continue  → salta esta vuelta y continúa con la siguiente
```

En un `for`, después de `continue`, se ejecuta la **actualización** del bucle y posteriormente se vuelve a comprobar la condición.

En un `while` o `do-while`, la ejecución pasa a la comprobación de la condición correspondiente.

>`continue` no detiene el bucle; únicamente **omite la iteración actual** y permite continuar con la siguiente.