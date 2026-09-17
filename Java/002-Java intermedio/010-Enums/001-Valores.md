### Valores 

Los **valores de un `enum`** son las constantes que se declaran dentro de la enumeración. Representan las **únicas opciones que puede tener ese tipo**.

Por ejemplo:

```java
enum Estado {
    PENDIENTE,
    EN_PROCESO,
    COMPLETADO,
    CANCELADO
}
```

En este caso, `PENDIENTE`, `EN_PROCESO`, `COMPLETADO` y `CANCELADO` son los valores del `enum`.

Cada uno de ellos es una **instancia del propio tipo `Estado`**. No son simplemente cadenas de texto ni números.

```java
Estado estado = Estado.PENDIENTE;
```

Esto significa que `estado` contiene una instancia concreta de `Estado`.

Una característica importante es que los valores de un `enum` están **definidos de antemano**. No podemos crear nuevos valores durante la ejecución del programa.

Además, cada valor es único dentro de ese `enum` y puede compararse directamente con los demás valores de la misma enumeración.

```java
if (estado == Estado.COMPLETADO) {
    // ...
}
```

Java también permite obtener todos los valores definidos en una enumeración mediante `values()`:

```
Estado[] estados = Estado.values();
```

Esto resulta útil cuando necesitamos recorrer todas las opciones disponibles.

> los valores de un `enum` son **instancias predefinidas del propio tipo enumerado**. Representan un conjunto cerrado de opciones que conocemos y definimos al crear el `enum`.