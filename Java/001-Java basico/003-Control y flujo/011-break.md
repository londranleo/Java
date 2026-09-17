## `break`

`break` se utiliza para **terminar inmediatamente la ejecución de la estructura de control en la que se encuentra**.

Cuando Java encuentra un `break`, deja de ejecutar el bucle o `switch` actual y continúa con la primera instrucción que aparece después de él.

En un bucle, permite **salir antes de que la condición normal del bucle deje de cumplirse**.

```java
for (int i = 0; i < 10; i++) {
    if (i == 5) {
        break;
    }
}
```

Cuando `i` llega a `5`, se ejecuta `break` y el `for` termina.

`break` también puede utilizarse dentro de un `switch` para evitar que la ejecución continúe con los siguientes `case`.

En el caso de **bucles anidados**, un `break` sin etiqueta termina únicamente el **bucle más interno** en el que se encuentra.

>`break` permite **salir inmediatamente** de un `for`, `while`, `do-while` o `switch`, sin esperar a que termine su funcionamiento normal.