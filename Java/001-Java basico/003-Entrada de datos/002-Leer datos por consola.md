**Leer datos por consola** consiste en permitir que el usuario introduzca información mediante el teclado mientras el programa está en ejecución. Estos datos pueden utilizarse posteriormente para realizar operaciones, tomar decisiones o almacenarse en variables.

Primero se crea un objeto `Scanner` asociado a la entrada estándar del programa, representada por `System.in`:

```java
Scanner entrada = new Scanner(System.in);
```

A partir de ese objeto se pueden utilizar diferentes métodos dependiendo del tipo de dato que se quiera leer:

| Método          | Tipo de dato       |
| --------------- | ------------------ |
| `nextInt()`     | `int`              |
| `nextLong()`    | `long`             |
| `nextDouble()`  | `double`           |
| `nextFloat()`   | `float`            |
| `nextBoolean()` | `boolean`          |
| `next()`        | Una palabra        |
| `nextLine()`    | Una línea completa |

Por ejemplo, para leer un número entero:

```java
int edad = entrada.nextInt();
```

El programa queda esperando hasta que el usuario introduzca un valor que pueda interpretarse como `int`.

Para leer texto completo se utiliza normalmente `nextLine()`:

```java
String nombre = entrada.nextLine();
```

La diferencia entre `next()` y `nextLine()` es importante: `next()` lee el siguiente elemento separado por espacios, mientras que `nextLine()` lee **toda la línea introducida**, incluyendo los espacios que pueda contener.

También hay que tener en cuenta que los métodos que leen tipos numéricos esperan que la entrada tenga un formato válido. Si el usuario introduce un valor que no puede convertirse al tipo solicitado, `Scanner` puede producir una excepción.

Cuando se termina de utilizar el `Scanner`, puede cerrarse mediante `close()`. Sin embargo, al hacerlo también se cierra `System.in`, por lo que hay que tenerlo en cuenta si el programa necesita volver a leer datos posteriormente.
