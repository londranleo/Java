## Operador ternario

El **operador ternario** permite evaluar una condición y seleccionar **uno de dos valores posibles** dependiendo de si dicha condición es verdadera o falsa.

Se denomina ternario porque trabaja con **tres operandos**:

```java
condición ? valor_si_true : valor_si_false
```

La condición debe producir un `boolean`. Si es `true`, se utiliza el valor situado después de `?`; si es `false`, se utiliza el valor situado después de `:`.

```java
int edad = 22;

String resultado = edad >= 18 ? "Mayor de edad" : "Menor de edad";
```

En este caso, como `edad >= 18` es `true`, `resultado` recibe `"Mayor de edad"`.

El operador ternario **produce un valor**, por lo que puede utilizarse directamente en una asignación, como argumento de un método o dentro de otra expresión.

También puede utilizarse con diferentes tipos de valores, siempre que los dos resultados sean compatibles con el contexto en el que se utiliza.

Su principal utilidad es expresar **decisiones sencillas que tienen dos posibles resultados**. Cuando la lógica contiene varias condiciones o necesita ejecutar varias instrucciones, una estructura `if-else` suele ser más apropiada y legible.

El operador ternario también puede anidarse, colocando otro operador ternario dentro de uno de los resultados. Sin embargo, abusar de esta posibilidad puede dificultar la lectura del código.

> El operador ternario es una forma compacta de obtener uno de dos valores según una condición. Su estructura es `condición ? valor1 : valor2` y, a diferencia de `if-else`, forma parte de una expresión porque devuelve un valor.