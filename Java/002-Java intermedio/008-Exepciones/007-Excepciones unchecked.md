### Excepciones unchecked

Las **unchecked exceptions** son excepciones que Java **no obliga a capturar ni a declarar** durante la compilación.

Normalmente pertenecen a `RuntimeException` o a alguna de sus subclases.

```
Throwable
   │
   └── Exception
        │
        └── RuntimeException
             ├── NullPointerException
             ├── IllegalArgumentException
             └── IndexOutOfBoundsException
```

La diferencia fundamental respecto a las checked exceptions es que el **compilador no exige que las gestionemos**.

Por ejemplo:

```java
String nombre = null;

nombre.length();
```

Aquí se produce una `NullPointerException`, pero Java no obliga a escribir un `try-catch` ni un `throws` para poder compilar el código.

### ¿Por qué no son obligatorias?

Las unchecked exceptions suelen representar problemas relacionados con **la lógica o el estado incorrecto del programa**.

Por ejemplo:

```java
int[] numeros = {1, 2, 3};

numeros[10];
```

El problema no suele ser algo externo que la aplicación deba esperar como parte normal de su funcionamiento. Normalmente indica que el código ha intentado realizar una operación incorrecta.

Por eso Java no obliga a capturar este tipo de excepciones.

```
Unchecked exception
        ↓
RuntimeException
        ↓
Java NO obliga a:
    ├── try-catch
    └── throws
```

Esto **no significa que no podamos manejarlas**. Podemos utilizar `try-catch` si tiene sentido para nuestra aplicación.

La diferencia es que Java **no nos obliga** a hacerlo.

### Checked vs unchecked

```
Checked
→ el compilador obliga a capturar o declarar

Unchecked
→ el compilador no obliga a capturar ni declarar
```

Una regla práctica importante es que las unchecked exceptions suelen indicar que **hay que corregir una condición o una lógica del programa**, en lugar de simplemente capturar la excepción y continuar.

>una unchecked exception es una excepción que normalmente deriva de `RuntimeException` y que **Java no obliga a capturar ni declarar**. Suele representar errores de programación o situaciones que podrían evitarse mediante una lógica correcta.