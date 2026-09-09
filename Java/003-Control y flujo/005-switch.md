## `switch`

`switch` es una estructura de control que permite **elegir qué código ejecutar dependiendo del valor de una expresión**.

Es especialmente útil cuando queremos comparar **un mismo valor con diferentes opciones**.

Su estructura básica es:

```java
switch (valor) {
    case opcion1:
        // código
        break;

    case opcion2:
        // código
        break;

    default:
        // código si ninguna opción coincide
}
```

Java evalúa el valor del `switch` y lo compara con cada `case`.

- Si encuentra un `case` que coincide, ejecuta su código.
- `break` hace que la ejecución salga del `switch`.
- `default` se ejecuta cuando ningún `case` coincide y es opcional.

Por ejemplo:

```java
int dia = 2;

switch (dia) {
    case 1:
        System.out.println("Lunes");
        break;
    case 2:
        System.out.println("Martes");
        break;
    default:
        System.out.println("Otro día");
}
```

En este caso, `dia` vale `2`, por lo que se ejecuta el `case 2`.

### `break`

`break` es importante en el `switch` tradicional porque indica que, después de ejecutar un `case`, debemos **salir del `switch`**.

Si no se utiliza, Java puede continuar ejecutando los siguientes `case`, aunque sus valores no coincidan. Este comportamiento se conoce como **fall-through**.

### `default`

`default` representa el caso en el que **ninguna de las opciones anteriores coincide**. No es obligatorio incluirlo.

### `switch` moderno

Las versiones modernas de Java también permiten utilizar `switch` como una **expresión**, pudiendo producir directamente un valor.

```java
String resultado = switch (dia) {
    case 1 -> "Lunes";
    case 2 -> "Martes";
    default -> "Otro";
};
```

Con esta sintaxis, `->` indica qué resultado corresponde a cada caso y no es necesario utilizar `break`.

> `switch` permite seleccionar una opción entre varios casos a partir del valor de una expresión. `case` representa cada posibilidad, `default` el caso que no coincide con ninguna y `break` permite terminar el `switch` tradicional.