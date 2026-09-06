Los **números aleatorios** son valores generados de manera que no podemos determinar directamente cuál será el siguiente valor a partir de los anteriores. En programación se utilizan para introducir variación o comportamientos no predecibles en situaciones como juegos, simulaciones, pruebas o selección de elementos.

En Java, una de las formas habituales de generar números aleatorios es mediante la clase `Random`, perteneciente al paquete `java.util`.

Primero se crea un objeto `Random`:

```
Random random = new Random();
```

A partir de este objeto se pueden generar valores de diferentes tipos mediante sus métodos. Por ejemplo, `nextInt()` genera un entero y `nextDouble()` genera un número decimal.

Cuando necesitamos que el número pertenezca a un **rango determinado**, podemos proporcionar un límite. Por ejemplo:

```
int numero = random.nextInt(10);
```

En este caso, el resultado estará entre `0` y `9`. El límite superior **no se incluye**.

Esto es importante para entender los rangos de generación:

```
nextInt(10)

mínimo → 0
máximo → 9
```

También es posible obtener un número dentro de un intervalo que comience en otro valor mediante operaciones matemáticas sobre el resultado generado.

### `Math.random()`

Java también proporciona `Math.random()`, que genera un valor `double` en un intervalo comprendido entre `0.0` incluido y `1.0` excluido.

```
double numero = Math.random();
```

Su resultado siempre cumple:

```
0.0 <= número < 1.0
```

`Math.random()` resulta sencillo cuando solo necesitamos un valor decimal aleatorio, mientras que `Random` proporciona métodos específicos para generar distintos tipos de valores y trabajar con rangos.

### Aleatoriedad y semillas

Los números generados por `Random` son **pseudoaleatorios**. Esto significa que son producidos mediante un algoritmo determinista que genera una secuencia que parece aleatoria.

El algoritmo utiliza un valor inicial llamado **semilla (seed)**. Si se utiliza la misma semilla y las mismas condiciones, se puede obtener la misma secuencia de valores. Esto resulta útil, por ejemplo, para reproducir resultados durante pruebas.

Por tanto, la aleatoriedad utilizada habitualmente en programación no debe confundirse necesariamente con una fuente de aleatoriedad física o impredecible.

>**Idea clave:** Java permite generar valores pseudoaleatorios mediante herramientas como `Random` y `Math.random()`. Al trabajar con rangos, hay que prestar especial atención a los límites, ya que normalmente el límite superior no forma parte de los valores posibles.