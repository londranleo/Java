## Clases abstractas

Una **clase abstracta** es una clase que sirve como **base para otras clases**, pero que no puede utilizarse directamente para crear objetos.

Se declara utilizando `abstract`:

```java
abstract class Animal {
}
```

Esto significa que no podemos hacer:

```java
Animal animal = new Animal(); // Error
```

La clase abstracta puede contener atributos y métodos normales, pero también puede tener **métodos abstractos**.

Un método abstracto es un método que **declara qué debe hacer una clase, pero no define cómo hacerlo**:

```java
abstract class Animal {

    abstract void hacerSonido();
}
```

Las clases que hereden de `Animal` tendrán que proporcionar la implementación:

```java
class Perro extends Animal {

    @Override
    void hacerSonido() {
        System.out.println("Guau");
    }
}
```

Así, la clase abstracta permite definir una estructura común y dejar determinados comportamientos para las clases hijas.

### ¿Por qué utilizar una clase abstracta?

Cuando varias clases tienen **características o comportamientos comunes**, podemos colocarlos en una clase abstracta y dejar que cada subclase implemente aquello que sea específico.

```
           Animal
          /      \
       Perro     Gato
        ↓          ↓
      Guau       Miau
```

Además, podemos utilizar una referencia del tipo abstracto:

```java
Animal animal = new Perro();
```

Esto permite utilizar el **polimorfismo** que vimos anteriormente.

> una clase abstracta es una clase base que no puede instanciarse directamente. Puede proporcionar código común y definir métodos abstractos que las clases hijas deben implementar.