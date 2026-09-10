### Métodos genéricos

Un **método genérico** es un método que utiliza uno o varios **parámetros de tipo** para poder trabajar con diferentes tipos de datos.

La diferencia importante respecto a una **clase genérica** es que un método genérico puede definir su propio parámetro de tipo **independientemente de la clase donde se encuentre**.

Por ejemplo:

```java
public static <T> void mostrar(T valor) {
    System.out.println(valor);
}
```

Aquí `<T>` indica que el método tiene un **parámetro de tipo propio**.

Podemos utilizar el mismo método con diferentes tipos:

```java
mostrar("Hola");
mostrar(25);
mostrar(3.14);
```

En cada llamada, Java determina qué tipo representa `T`.

```
mostrar("Hola")
→ T = String

mostrar(25)
→ T = Integer

mostrar(3.14)
→ T = Double
```

### ¿Dónde se declara el tipo?

En un método genérico, el parámetro de tipo se declara **antes del tipo de retorno**:

```java
<T> void metodo(T valor)
```

Ese `<T>` es lo que indica que el método es genérico.

Esto es diferente de simplemente utilizar un tipo genérico que ya pertenece a la clase.

La principal ventaja es la **reutilización**: podemos definir una operación una sola vez y permitir que funcione con diferentes tipos manteniendo la comprobación de tipos del compilador.

Un método genérico también puede **devolver un tipo genérico**:

```java
public static <T> T obtener(T valor) {
    return valor;
}
```

En este caso, el tipo que devuelve el método está relacionado con el tipo recibido.

Los métodos genéricos pueden aparecer tanto dentro de **clases genéricas como dentro de clases normales**. No es necesario que la clase sea genérica para que uno de sus métodos lo sea.

>un método genérico permite definir una operación que puede trabajar con **diferentes tipos**, utilizando parámetros de tipo propios del método y manteniendo la seguridad de tipos.