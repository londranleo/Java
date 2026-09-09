## Polimorfismo

El **polimorfismo** permite que una misma referencia pueda utilizarse para trabajar con **objetos de diferentes clases**, y que cada objeto responda de acuerdo con su propia implementación.

En Java, suele aparecer junto con la **herencia** y la **sobreescritura de métodos**.

Por ejemplo:

```java
class Animal {
    void hacerSonido() {
        System.out.println("Sonido");
    }
}

class Perro extends Animal {
    @Override
    void hacerSonido() {
        System.out.println("Guau");
    }
}

class Gato extends Animal {
    @Override
    void hacerSonido() {
        System.out.println("Miau");
    }
}
```

Podemos utilizar una referencia de tipo `Animal` para guardar objetos de diferentes subclases:

```java
Animal animal1 = new Perro();
Animal animal2 = new Gato();
```

Aunque las dos referencias son de tipo `Animal`, los objetos reales son diferentes.

Si llamamos al mismo método:

```java
animal1.hacerSonido();
animal2.hacerSonido();
```

se ejecuta:

```java
animal1 → Guau
animal2 → Miau
```

Esto ocurre porque Java determina **en tiempo de ejecución** qué implementación sobrescrita corresponde al objeto real.

### ¿Por qué es útil?

El polimorfismo permite escribir código que trabaja con un **tipo general**, sin tener que conocer exactamente qué subclase está utilizando.

Por ejemplo, un método podría recibir cualquier `Animal`:

```java
void hacerSonar(Animal animal) {
    animal.hacerSonido();
}
```

Podemos pasarle un `Perro`, un `Gato` u otra subclase de `Animal`, y cada uno ejecutará su propia implementación.

La idea fundamental es:

```
Referencia → tipo general
Objeto     → tipo concreto
Método     → comportamiento del objeto concreto
```

>el polimorfismo permite tratar objetos de diferentes subclases como objetos de un tipo común, manteniendo el comportamiento específico de cada objeto.