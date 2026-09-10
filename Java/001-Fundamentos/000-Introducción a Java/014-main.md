# main

**`main`** es el método especial desde el que arranca la ejecución de cualquier programa Java. Cuando ejecutas un programa (por ejemplo, con `java Main`), la JVM busca este método dentro de la clase indicada y comienza a ejecutar las instrucciones a partir de él.

Su forma estándar es la siguiente:

```java
public class Main {
    public static void main(String[] args) {
        // instrucciones del programa
    }
}
```

Cada palabra de su declaración tiene un motivo concreto:

- **`public`**: hace que el método sea accesible desde fuera de la clase, ya que la JVM necesita poder llamarlo desde el exterior del programa.
- **`static`**: permite que la JVM ejecute el método sin necesidad de crear antes un objeto de la clase. Es el punto de partida, así que todavía no existe ningún objeto creado.
- **`void`**: indica que el método no devuelve ningún valor.
- **`main`**: es el nombre exacto que la JVM busca para saber por dónde empezar. Debe llamarse así, sin variaciones.
- **`String[] args`**: es un array de texto que permite recibir argumentos desde la línea de comandos al ejecutar el programa (por ejemplo, `java Main hola`, donde `"hola"` llegaría dentro de `args`). Si no se necesitan argumentos, este array simplemente queda vacío.

Un programa Java puede tener varias clases, pero solo una de ellas (la que se indique al ejecutar) necesita contener el método `main` que se vaya a utilizar como punto de entrada. Si una clase no tiene `main`, no puede ejecutarse directamente, aunque sí puede ser utilizada por otras clases que sí lo tengan.

Cualquier código escrito dentro del cuerpo de `main` se ejecuta en orden, de arriba hacia abajo, en el momento en el que se lanza el programa.