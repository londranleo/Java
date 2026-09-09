## Interfaces

Una **interfaz** define un conjunto de **métodos que una clase debe proporcionar**, estableciendo un contrato sobre el comportamiento que debe tener.

Se declara con `interface`:

```java
interface Animal {
    void hacerSonido();
}
```

Una clase utiliza una interfaz mediante `implements`:

```java
class Perro implements Animal {

    @Override
    public void hacerSonido() {
        System.out.println("Guau");
    }
}
```

La clase `Perro` está obligada a implementar `hacerSonido()` porque ese método forma parte del contrato de `Animal`.

### Interfaz vs clase

Una interfaz se centra principalmente en **qué puede hacer un objeto**, mientras que una clase puede definir tanto **qué datos tiene como cómo funciona internamente**.

Por ejemplo:

```
Animal
   ↓
"debe poder hacer un sonido"

Perro
   ↓
"cómo hace ese sonido → Guau"

Gato
   ↓
"cómo hace ese sonido → Miau"
```

Una clase puede **implementar varias interfaces**:

```
class Perro implements Animal, Mascota {
}
```

Esto es diferente de la herencia entre clases, donde una clase solo puede extender directamente **una única clase**.

Las interfaces también pueden contener implementaciones mediante métodos `default` y `static`, por lo que no deben entenderse simplemente como una lista de métodos vacíos.

Además, podemos utilizar una interfaz como tipo de referencia:

```java
Animal animal = new Perro();
```

Esto permite utilizar **polimorfismo**: el código trabaja con el contrato `Animal`, mientras que el objeto concreto determina su comportamiento.

>una interfaz define un **contrato de comportamiento**. Las clases que la implementan se comprometen a proporcionar ese comportamiento y pueden implementar varias interfaces.