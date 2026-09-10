# Argumentos de `main`

Los **argumentos de `main`** son valores de texto que se pueden pasar a un programa Java **desde fuera**, en el momento de ejecutarlo, sin necesidad de escribirlos dentro del propio código.

Se reciben a través del parámetro `String[] args` del método `main`:

```java
public static void main(String[] args) {
    // args contiene los valores recibidos
}
```

`args` es un **array de String**: cada valor que se pase al ejecutar el programa se guarda como un elemento de ese array, en el mismo orden en el que se escriban.

Estos valores se indican al ejecutar el programa desde la línea de comandos, después del nombre de la clase:

```text
java Main hola 25
```

En este caso, `args` contendría dos elementos: `args[0]` sería `"hola"` y `args[1]` sería `"25"`. Es importante tener en cuenta que **todos los valores llegan como texto (`String`)**, aunque parezcan números. Si se necesita utilizar `"25"` como un número, hay que convertirlo explícitamente, por ejemplo con `Integer.parseInt(args[0])`.

Si al ejecutar el programa no se pasa ningún argumento, `args` no será `null`, sino un array vacío (de longitud `0`). Intentar acceder a una posición que no existe (por ejemplo, `args[0]` cuando no se pasó ningún argumento) provocaría un error en tiempo de ejecución.

Los argumentos de `main` son útiles cuando se quiere que un programa reciba información variable cada vez que se ejecuta, sin tener que modificar el código fuente para ello.