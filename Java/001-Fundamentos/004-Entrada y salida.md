## Entrada y salida

La **entrada y salida (I/O, Input/Output)** es la comunicación de un programa con el exterior.

- **Entrada (Input)** → datos que el programa **recibe**.
- **Salida (Output)** → información que el programa **envía o muestra**.

```java
Entrada → Programa → Salida
```

Por ejemplo, un programa puede recibir un nombre escrito por el usuario y después mostrar un mensaje.

### Salida

En Java, la salida más habitual por consola se realiza mediante `System.out`.

```java
System.out.println("Hola");
```

`println` muestra el contenido y después realiza un salto de línea.

También existen:

```java
System.out.print("Hola");
System.out.printf("Edad: %d", 22);
```

La diferencia es que `print` **no añade un salto de línea**, mientras que `println` sí. `printf` permite mostrar información utilizando un **formato especificado**.

### Entrada

Para recibir datos desde la consola podemos utilizar `Scanner`.

```java
Scanner scanner = new Scanner(System.in);

String nombre = scanner.nextLine();
```

`System.in` representa la **entrada estándar**, normalmente el teclado cuando ejecutamos el programa desde una consola.

`Scanner` permite interpretar los datos recibidos según el tipo que necesitemos:

```java
nextLine() → String
nextInt()  → int
nextDouble() → double
nextBoolean() → boolean
```

La entrada no tiene por qué proceder únicamente del teclado. Un programa también puede recibir datos desde **archivos, redes, bases de datos, interfaces gráficas u otras fuentes**. En este apartado nos centramos en la entrada y salida básica por consola.

**Idea clave:** la entrada permite que un programa **reciba información** y la salida permite que **comunique información**. En la consola, Java utiliza principalmente `System.in` para entrada y `System.out` para salida.