# Bytecode

El **bytecode** es el resultado de compilar código fuente Java. Es un conjunto de instrucciones en un formato intermedio, que no está escrito en un lenguaje que el procesador de tu ordenador entienda directamente, pero tampoco es legible para humanos como el código fuente original.

Cuando compilas un archivo `.java` con `javac`, el compilador no genera código específico para Windows, Linux o macOS, sino que genera bytecode, guardado en archivos con extensión **`.class`**. Este bytecode es el mismo independientemente del sistema operativo en el que se haya compilado.

La responsable de ejecutar ese bytecode es la **JVM**. Cuando ejecutas un programa Java, la JVM lee el archivo `.class`, interpreta sus instrucciones y las traduce a instrucciones que el sistema operativo y el hardware puedan entender y ejecutar.

Este formato intermedio es precisamente lo que permite que Java sea un lenguaje **multiplataforma**: como el bytecode es siempre el mismo, un programa compilado una sola vez puede ejecutarse en cualquier sistema que tenga una JVM instalada, sin necesidad de volver a compilarlo para cada sistema operativo.

El bytecode no es simplemente código fuente sin formato ni tampoco código máquina directo del procesador: es un paso intermedio, pensado específicamente para que la JVM pueda interpretarlo y ejecutarlo de forma eficiente.