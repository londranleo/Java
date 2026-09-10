### Errores y excepciones

En Java, **errores y excepciones son problemas que pueden producirse durante la ejecución de un programa**, pero representan situaciones diferentes.

La diferencia principal está en **qué tipo de problema representan y si normalmente el programa puede recuperarse de él**.

### Errores (`Error`)

Los `Error` representan problemas graves relacionados normalmente con el **funcionamiento de la propia máquina virtual de Java (JVM)** o con recursos que el programa no puede manejar normalmente.

No están pensados para que una aplicación los capture y continúe funcionando como si nada.

Por ejemplo, un agotamiento de la memoria o de la pila de ejecución puede producir un `Error`.

```java
StackOverflowError
OutOfMemoryError
```

Estos problemas normalmente indican que existe una situación grave que debe corregirse en el programa, en su configuración o en el entorno de ejecución.

### Excepciones (`Exception`)

Las excepciones representan situaciones anómalas que pueden producirse durante la ejecución de un programa y que **el programa puede detectar y gestionar**.

Por ejemplo, intentar convertir un texto que no representa un número puede provocar una excepción:

```java
Integer.parseInt("abc");
```

Java puede detectar esta situación y lanzar una excepción que el programa puede tratar.

Las excepciones forman parte del mecanismo normal de Java para comunicar que **una operación no ha podido realizarse como se esperaba**.

### Diferencia conceptual

```
Throwable
│
├── Error
│   └── Problemas graves del entorno/JVM
│
└── Exception
    └── Situaciones que la aplicación puede gestionar
```

Ambos pertenecen a la jerarquía de `Throwable`, pero tienen propósitos diferentes.

No significa que **todo `Error` sea imposible de capturar** ni que **toda `Exception` pueda solucionarse**. La diferencia está principalmente en cómo se clasifican y en la intención de su mecanismo de tratamiento.

>un `Error` representa normalmente un problema grave que la aplicación no debería intentar gestionar como una situación normal, mientras que una `Exception` representa una situación excepcional que el programa puede detectar y manejar.