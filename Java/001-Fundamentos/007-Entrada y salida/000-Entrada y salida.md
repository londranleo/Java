# Entrada y salida

En Java, la **salida** es mostrar información por pantalla, y la **entrada** es recibir información que escribe el usuario mientras el programa está en ejecución.

## Salida: System.out

Para mostrar texto por pantalla se usa `System.out`, que representa la consola. Los métodos más comunes son:

```java
System.out.println("Hola mundo"); // muestra el texto y salta de línea
System.out.print("Hola mundo");   // muestra el texto sin saltar de línea
```

`println` añade un salto de línea al final, por lo que lo siguiente que se muestre aparecerá en la línea de abajo. `print` no lo hace, así que si se llama varias veces seguidas, el texto queda todo en la misma línea.

## Entrada: System.in y Scanner

`System.in` es el flujo que representa la entrada de datos (normalmente el teclado), pero trabajar con él directamente es incómodo. Por eso se usa la clase `Scanner`, que simplifica la lectura de datos que escribe el usuario.

Para usarla, primero hay que importarla y crear un objeto `Scanner` conectado a `System.in`:

```java
import java.util.Scanner;

Scanner sc = new Scanner(System.in);
```

Este objeto `sc` es el que se utiliza después para leer lo que el usuario escribe.

### Entrada de texto

Para leer una línea completa de texto se usa `nextLine()`:

```java
String nombre = sc.nextLine();
```

El programa se detiene en esa línea y espera a que el usuario escriba algo y pulse Enter. Todo lo que haya escrito (incluidos los espacios) se guarda en la variable.

### Entrada numérica

Para leer números existen métodos específicos según el tipo de dato:

```java
int edad = sc.nextInt();
double altura = sc.nextDouble();
```

Estos métodos leen solo el número, no la línea completa. Si el usuario escribe texto donde se espera un número, el programa lanza un error.
### printf

`printf` permite construir una salida con un formato específico, usando un texto con marcadores especiales que luego se sustituyen por valores:

```java
int edad = 25;
System.out.printf("Tienes %d años%n", edad);
```

Los marcadores más comunes son:

- `%d` para números enteros.
- `%f` para números decimales.
- `%s` para texto (cadenas).
- `%n` para salto de línea (equivalente a pulsar Enter).

También se puede controlar cuántos decimales mostrar en un número decimal:

```java
double precio = 19.5;
System.out.printf("Precio: %.2f%n", precio); // Precio: 19.50
```

El `.2` indica que se quieren mostrar exactamente 2 decimales, redondeando si es necesario. Este control de formato es especialmente útil cuando se trabaja con dinero, medidas u otros datos donde la cantidad de decimales importa.