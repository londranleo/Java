# Compilación

La **compilación** es el proceso mediante el cual el código fuente que escribes (archivos `.java`) se transforma en **bytecode** (archivos `.class`), un formato intermedio que la JVM puede entender y ejecutar.

Este proceso lo realiza el **compilador de Java**, llamado `javac`, que forma parte del JDK. Al compilar un archivo `.java`, `javac` revisa que el código cumpla correctamente la sintaxis y las reglas del lenguaje Java. Si encuentra algún error (por ejemplo, una instrucción mal escrita o un tipo de dato incorrecto), la compilación falla y se muestra un mensaje indicando el problema, sin generar el archivo `.class`.

Si el código es correcto, `javac` genera un archivo `.class` por cada clase compilada, conteniendo el bytecode correspondiente. Por ejemplo:

```text
javac Main.java
```

Esto generaría un archivo `Main.class` a partir de `Main.java`.

Es importante diferenciar la compilación de la ejecución: compilar solo transforma el código fuente en bytecode, pero no lo ejecuta. Para ejecutar ese bytecode, es necesario utilizar la JVM (por ejemplo, mediante el comando `java Main`), que interpretará el archivo `.class` y llevará a cabo las instrucciones del programa.

Gracias a este proceso de compilación a bytecode (en lugar de compilar directamente a código específico de un sistema operativo), el mismo archivo `.class` puede ejecutarse en cualquier sistema que tenga una JVM instalada, sin necesidad de volver a compilarlo.