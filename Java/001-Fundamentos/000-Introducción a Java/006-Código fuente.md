# Código fuente

El **código fuente** es el texto que escribes tú, como programador, siguiendo las reglas y la sintaxis del lenguaje Java. Es, básicamente, las instrucciones legibles por humanos que indican qué debe hacer el programa.

En Java, el código fuente se guarda en archivos con extensión **`.java`**. Por ejemplo, un archivo llamado `Main.java` contendría código como este:

```java
public class Main {
    public static void main(String[] args) {
        int edad = 25;
    }
}
```

Este código, tal y como está escrito, **no puede ejecutarlo directamente el ordenador**. Antes debe pasar por un proceso de compilación, en el que el compilador (`javac`) transforma el código fuente en bytecode (`.class`), que sí puede ser entendido y ejecutado por la JVM.

Cada archivo `.java` normalmente contiene el código fuente de una clase, y el nombre del archivo debe coincidir con el nombre de la clase pública que contiene (por ejemplo, `Main.java` debe contener la clase `Main`).

El código fuente es el punto de partida de cualquier programa Java: es lo que escribes, lo que editas, lo que revisas cuando corriges errores, y lo que finalmente se convierte en un programa ejecutable a través del proceso de compilación.