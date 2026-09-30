Una constante en Java es una variable cuyo valor No piede modificarse una vez que se ha inicializado.

Las constantes se utilizan para valores que sabemos que no cambiaran a lo larofo de la ejecucion del programa.

En Java, las constantes se crean utilizando la palabra clave `final`. Al declarar una variable como `final`, solo puede recibir una asignación válida una vez.

```java
// Sintaxis 
final tipo nombreConstante = valor;
```

```java
//Ejemplos de constantes
final int diasEnSemanas = 7;
final double PI = 3.14159;
final Stirng mensajeBienvenida = "Bienvenido a Java"
```

>**Tambien podemos usar `var` para definir una constante**


`final` impide cambiar **la referencia o el valor almacenado en la variable**, pero no significa necesariamente que el objeto al que apunta sea inmutable.
