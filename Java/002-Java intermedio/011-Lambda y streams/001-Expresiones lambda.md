### Expresiones lambda

Una **expresión lambda** es una forma compacta de representar el **comportamiento de un método** sin tener que crear una clase para implementarlo.

Las lambdas están directamente relacionadas con las **interfaces funcionales**: una lambda proporciona la implementación del único método abstracto de una interfaz funcional.

Por ejemplo:

```java
Operacion suma = (a, b) -> a + b;
```

Aquí la lambda:

```java
(a, b) -> a + b
```

representa el comportamiento del método `ejecutar()` de la interfaz `Operacion`.

Conceptualmente:

```
Interfaz funcional
       ↓
método abstracto
       ↓
expresión lambda
       ↓
comportamiento
```

La estructura general de una lambda es:

```java
(parámetros) -> expresión
```

o, cuando necesita varias instrucciones:

```java
(parámetros) -> {
    // instrucciones
}
```

La flecha `->` separa los **parámetros** de la **operación que debe realizarse**.

Una lambda **no es una clase ni un método independiente**. Es una expresión que representa una implementación de una interfaz funcional.

Esto permite tratar determinados comportamientos como valores y pasarlos a otros métodos. Esta característica es especialmente importante en las operaciones de colecciones y, posteriormente, en **Streams**.

Por ejemplo, podemos indicar qué operación queremos realizar sobre los elementos de una colección sin tener que crear una clase específica para representar esa operación.

### Lambda y tipos

Java mantiene la comprobación de tipos. El compilador utiliza el **tipo de la interfaz funcional** para determinar qué parámetros recibe la lambda y qué resultado debe producir.

```java
Operacion operacion = (a, b) -> a + b;
```

Como `operacion` es de tipo `Operacion`, Java sabe qué representa `a`, qué representa `b` y qué debe devolver la lambda.

> una expresión lambda permite representar de forma compacta un **comportamiento** y utilizarlo como un valor. En Java, las lambdas se utilizan principalmente para proporcionar implementaciones de **interfaces funcionales** y son una pieza fundamental de Streams.