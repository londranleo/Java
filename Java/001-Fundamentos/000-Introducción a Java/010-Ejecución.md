# Ejecución

La **ejecución** es el proceso mediante el cual la JVM lee el bytecode (archivos `.class`) y lleva a cabo las instrucciones del programa, haciendo que este realmente funcione.

Para ejecutar un programa Java, se utiliza el comando `java`, indicando la clase que contiene el método `main`, que es el punto de entrada del programa:

```text
java Main
```

Al ejecutar este comando, la JVM localiza el archivo `Main.class`, interpreta su bytecode y comienza a ejecutar las instrucciones a partir del método `main`, que es donde arranca cualquier programa Java.

Durante la ejecución, la JVM no se limita a interpretar instrucciones una por una: también gestiona tareas como la reserva y liberación de memoria mediante el recolector de basura, y en muchos casos optimiza partes del código en tiempo real para mejorar el rendimiento.

Es importante distinguir la ejecución de la compilación: la compilación transforma el código fuente en bytecode una sola vez, mientras que la ejecución es el momento en el que ese bytecode se interpreta y se lleva a cabo, cada vez que se ejecuta el programa. Un mismo archivo `.class`, una vez compilado, puede ejecutarse tantas veces como se desee sin necesidad de volver a compilarlo.