## Clases genéricas

Una **clase genérica** es una clase que utiliza uno o varios **parámetros de tipo** para poder trabajar con diferentes tipos de datos sin tener que crear una clase diferente para cada uno.

La idea es que la clase no necesita conocer desde el principio qué tipo concreto va a utilizar. Ese tipo se especifica cuando **creamos un objeto de la clase**.

Por ejemplo:

```java
class Caja<T> {
    private T contenido;

    public void guardar(T contenido) {
        this.contenido = contenido;
    }

    public T obtener() {
        return contenido;
    }
}
```

Aquí `T` representa un **tipo que será determinado posteriormente**.

Podemos utilizar la misma clase con diferentes tipos:

```java
Caja<String> cajaTexto = new Caja<>();
Caja<Integer> cajaNumero = new Caja<>();
```

En el primer caso, `T` representa `String`. En el segundo, `T` representa `Integer`.

```
Caja<T>
   │
   ├── Caja<String>
   │      T → String
   │
   └── Caja<Integer>
          T → Integer
```

Esto permite que la clase sea **reutilizable** sin perder seguridad de tipos.

Una característica importante es que el tipo genérico se utiliza dentro de la propia definición de la clase. Puede aparecer como tipo de atributos, parámetros de métodos y valores de retorno.

Además, el compilador comprueba que utilicemos la clase con el tipo indicado correctamente:

```java
Caja<String> caja = new Caja<>();

caja.guardar("Hola");
caja.guardar(10); // Error
```

La clase sigue siendo la misma; lo que cambia es el **tipo que representa `T`** en cada utilización.

Una clase puede tener más de un parámetro genérico:

```java
class Pareja<K, V> {
    private K clave;
    private V valor;
}
```

Esto permite representar relaciones entre diferentes tipos, igual que ocurre con `Map<K, V>`.

>una clase genérica es una clase cuyo código está parametrizado mediante uno o varios **tipos**, permitiendo reutilizar la misma estructura con diferentes tipos de datos manteniendo la seguridad de tipos.