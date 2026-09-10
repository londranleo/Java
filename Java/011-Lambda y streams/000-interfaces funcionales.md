## Interfaces funcionales

Una **interfaz funcional** es una interfaz que tiene **exactamente un método abstracto**.

Su importancia en Java está en que permite representar una **operación o comportamiento que puede pasarse como dato**, algo fundamental para entender las expresiones **lambda** y los **Streams**.

Por ejemplo:

```java
@FunctionalInterface
interface Operacion {
    int ejecutar(int a, int b);
}
```

Esta interfaz es funcional porque tiene un único método abstracto: `ejecutar()`.

El concepto importante no es el nombre del método ni sus parámetros, sino que exista **un solo método abstracto que deba implementarse**.

### `@FunctionalInterface`

Java proporciona la anotación `@FunctionalInterface` para indicar que una interfaz está destinada a ser funcional.

```java
@FunctionalInterface
interface Operacion {
    int ejecutar(int a, int b);
}
```

La anotación no convierte una interfaz en funcional. La interfaz ya debe cumplir la regla de tener un único método abstracto. La anotación sirve para que el compilador pueda comprobar que esa condición se mantiene.

Una interfaz funcional **puede tener métodos `default` y `static`**. Lo que debe existir exactamente es **un solo método abstracto**.

### ¿Por qué son importantes?

Las interfaces funcionales permiten describir **qué operación queremos realizar sin tener que definir una clase completa para representarla**.

Esto es precisamente lo que aprovechan las expresiones lambda.

```java
Operacion suma = (a, b) -> a + b;
```

Aquí la lambda proporciona la implementación del único método abstracto de `Operacion`.

Conceptualmente:

```
Interfaz funcional
       ↓
un método abstracto
       ↓
lambda
       ↓
implementación del comportamiento
```

Java ya proporciona varias interfaces funcionales muy utilizadas, como `Predicate`, `Function`, `Consumer` y `Supplier`. Estas forman parte de `java.util.function` y serán importantes cuando avancemos hacia lambdas y Streams.

>una interfaz funcional es una interfaz con **un único método abstracto**. Su importancia está en que permite representar comportamientos y utilizarlos mediante **expresiones lambda**, que serán la base del siguiente tema.