# Cómo funciona un programa Java desde que se escribe hasta que se ejecuta

Un programa Java pasa por varias etapas desde que se escribe hasta que finalmente funciona en un ordenador.

Todo comienza con el **código fuente**: el texto que escribes en un archivo `.java`, siguiendo la sintaxis del lenguaje Java. Este código es legible para las personas, pero no puede ejecutarlo directamente el ordenador.

```java
public class Main {
    public static void main(String[] args) {
        int edad = 25;
    }
}
```

El siguiente paso es la **compilación**. El compilador de Java (`javac`), incluido en el JDK, revisa que el código fuente sea correcto según las reglas del lenguaje. Si todo está bien, transforma ese archivo `.java` en un archivo `.class`, que contiene **bytecode**: un formato intermedio que no es directamente entendible por el procesador, pero que tampoco es texto legible como el código original. Si el compilador encuentra errores, la compilación falla y no se genera el archivo `.class`.

```text
javac Main.java   →   Main.class
```

Una vez generado el bytecode, llega el momento de la **ejecución**. Al ejecutar el programa (por ejemplo, con el comando `java Main`), entra en juego la **JVM** (Java Virtual Machine). La JVM lee el archivo `.class`, interpreta su bytecode y lo traduce, en tiempo real, a instrucciones que el sistema operativo y el hardware del ordenador pueden entender y llevar a cabo. Durante este proceso, la JVM también se encarga de tareas como la gestión automática de memoria mediante el recolector de basura.

Gracias a que la compilación genera bytecode (y no código específico de un sistema operativo), un mismo archivo `.class` puede ejecutarse en cualquier ordenador que tenga una JVM instalada, sin necesidad de volver a compilarlo. Esto es lo que hace que Java sea un lenguaje multiplataforma, resumido en la idea de **"escribe una vez, ejecuta en cualquier lugar"**.

En resumen, el recorrido de un programa Java sigue siempre esta secuencia: código fuente (`.java`) → compilación (`javac`) → bytecode (`.class`) → ejecución (JVM).