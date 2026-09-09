## Composición

La **composición** consiste en crear una clase que **contiene objetos de otras clases** para utilizarlos como parte de su funcionamiento.

En lugar de que una clase herede de otra, una clase **tiene** un objeto de otra clase.

Por ejemplo:

```java
class Motor {
    void arrancar() {
        System.out.println("Motor arrancado");
    }
}

class Coche {
    private Motor motor;

    Coche() {
        motor = new Motor();
    }
}
```

Aquí `Coche` no hereda de `Motor`.

La relación es:

```
Coche
  │
  └── tiene un → Motor
```

Esto se conoce como una relación **"tiene un" (has-a)**.

En cambio, la herencia representa normalmente una relación **"es un" (is-a)**:

```
Perro → es un → Animal
Coche → tiene un → Motor
```

### ¿Por qué utilizar composición?

La composición permite construir objetos complejos **combinando otros objetos**.

Además, una clase puede utilizar diferentes componentes sin tener que convertirse en una subclase de ellos.

Por ejemplo, `Coche` puede utilizar un `Motor`, un `Freno`, una `Rueda`, etc., cada uno encargado de una responsabilidad concreta.

La composición también ayuda a mantener las clases más independientes y facilita cambiar un componente sin tener que modificar toda la jerarquía de herencia.

> la composición consiste en que una clase **tiene y utiliza objetos de otras clases**. Representa una relación de **"tiene un"**, mientras que la herencia representa una relación de **"es un"**.