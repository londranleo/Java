### Métodos 

Un `enum` puede tener **métodos**, igual que una clase normal. Esto permite que la enumeración no solo represente un conjunto de valores, sino que también pueda contener **comportamiento relacionado con esos valores**.

Por ejemplo:

```java
enum Estado {
    PENDIENTE,
    COMPLETADO;

    public boolean estaFinalizado() {
        return this == COMPLETADO;
    }
}
```

Cada valor del `enum` puede utilizar los métodos definidos dentro de la enumeración:

```java
Estado estado = Estado.COMPLETADO;

estado.estaFinalizado();
```

El método pertenece al tipo `Estado`, por lo que puede utilizarse desde cualquiera de sus valores.

Los `enum` también tienen **métodos proporcionados por Java**, como `values()` y `valueOf()`.

`values()` permite obtener todos los valores definidos en el `enum`:

```java
Estado[] estados = Estado.values();
```

`valueOf()` permite obtener un valor del `enum` a partir de su nombre:

```java
Estado estado = Estado.valueOf("COMPLETADO");
```

Si el nombre proporcionado no corresponde con ningún valor existente, `valueOf()` produce una excepción.

Una característica importante es que los métodos de un `enum` pueden utilizar `this` para referirse al **valor concreto** sobre el que se está ejecutando el método.

Por tanto, un `enum` no debe entenderse simplemente como una colección de constantes. Es un **tipo completo**, capaz de contener valores, atributos, métodos y comportamiento propio.

>los métodos permiten que un `enum` tenga **comportamiento propio**, haciendo que sus valores no sean únicamente constantes, sino objetos capaces de realizar operaciones relacionadas con su significado.