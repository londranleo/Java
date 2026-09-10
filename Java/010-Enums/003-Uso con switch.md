### Uso de `enum` con `switch`

Los `enum` se utilizan frecuentemente junto con `switch` cuando necesitamos **ejecutar diferentes comportamientos dependiendo del valor de una enumeración**.

Esto resulta especialmente útil porque `switch` puede trabajar directamente con los valores del `enum`, sin necesidad de convertirlos a números o cadenas.

```java
enum Estado {
    PENDIENTE,
    EN_PROCESO,
    COMPLETADO
}

Estado estado = Estado.EN_PROCESO;

switch (estado) {
    case PENDIENTE:
        // ...
        break;

    case EN_PROCESO:
        // ...
        break;

    case COMPLETADO:
        // ...
        break;
}
```

La idea es que el `switch` recibe un valor de tipo `Estado` y cada `case` representa uno de los valores definidos dentro de ese `enum`.

```
Estado
   ↓
EN_PROCESO
   ↓
switch
   ├── PENDIENTE
   ├── EN_PROCESO  ← se ejecuta este caso
   └── COMPLETADO
```

Una ventaja importante es que el código queda **más claro y seguro** que si utilizáramos números o cadenas para representar estados.

Por ejemplo, utilizar:

```java
int estado = 2;
```

no deja claro qué significa `2`.

Mientras que:

```
Estado estado = Estado.COMPLETADO;
```

expresa directamente el significado del valor.

Además, cuando utilizamos un `enum`, el compilador conoce cuáles son los valores pertenecientes a ese tipo, lo que ayuda a evitar errores relacionados con valores inválidos.

>combinar `enum` con `switch` permite **seleccionar un comportamiento según un valor predefinido**, haciendo que el código sea más claro, seguro y fácil de mantener.