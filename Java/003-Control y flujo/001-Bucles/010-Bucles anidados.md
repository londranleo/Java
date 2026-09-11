## Bucles anidados

Los **bucles anidados** son bucles que se encuentran **dentro de otro bucle**. El bucle exterior controla las repeticiones principales y, en cada una de ellas, se ejecuta el bucle interior.

```java
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 2; j++) {
        System.out.println(i + " " + j);
    }
}
```

El funcionamiento es importante: **por cada vuelta del bucle exterior, el bucle interior realiza todas sus vueltas** antes de que el exterior continúe con la siguiente.

Por ejemplo, si el exterior realiza 3 vueltas y el interior 2, el código del interior se ejecutará **3 × 2 = 6 veces**.

Los bucles pueden anidarse utilizando `for`, `while` o `do-while`, e incluso pueden combinarse entre ellos.

Son especialmente útiles cuando necesitamos trabajar con estructuras que tienen **más de una dimensión**, como arrays bidimensionales, tablas o matrices.

También hay que tener en cuenta que cada bucle mantiene su propio control. Una variable utilizada para controlar un bucle no tiene por qué ser la misma que controla el otro.

>un bucle anidado es un bucle dentro de otro. El bucle interior se completa en cada repetición del exterior, por lo que el número total de ejecuciones depende de las repeticiones de ambos bucles.