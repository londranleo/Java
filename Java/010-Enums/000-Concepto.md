## Concepto

Un **`enum` (enumeración)** es un tipo especial de Java que permite definir un **conjunto fijo y limitado de valores posibles**.

La idea principal es que, en lugar de representar determinados estados o categorías mediante valores que podrían ser incorrectos, podemos definir **exactamente qué valores son válidos**.

Por ejemplo:

```java
enum Estado {
    PENDIENTE,
    EN_PROCESO,
    COMPLETADO,
    CANCELADO
}
```

En este caso, `Estado` solo puede representar los valores que hemos definido dentro de la enumeración.

```
Estado
├── PENDIENTE
├── EN_PROCESO
├── COMPLETADO
└── CANCELADO
```

Esto hace que un `enum` sea especialmente útil cuando tenemos un conjunto de opciones que **no debería cambiar durante la ejecución del programa**.

Un `enum` es más que una lista de constantes. En Java, cada valor de un `enum` es una **instancia del propio tipo enumerado**. Por eso un `enum` puede tener atributos, métodos y constructores.

Otra característica importante es que Java conoce todos los valores que pertenecen a la enumeración. Esto permite trabajar con ellos de manera segura y evita utilizar valores arbitrarios que no formen parte del conjunto definido.

Por ejemplo:

```java
Estado estado = Estado.PENDIENTE;
```

Aquí `estado` no puede contener cualquier valor, sino un valor perteneciente a `Estado`.

### ¿Para qué sirve?

Los `enum` son apropiados para representar conceptos con un **número cerrado de posibilidades**:

```
enum Dia {
    LUNES,
    MARTES,
    MIERCOLES
}
```

También pueden representar estados, categorías, niveles, tipos, permisos, etc.

>un `enum` es un **tipo especial que define un conjunto fijo de valores**, proporcionando una forma segura y clara de representar opciones que están limitadas a un conjunto conocido.