## Herencia

La **herencia** permite crear una clase nueva a partir de otra clase, haciendo que la nueva clase **reciba sus atributos y métodos**.

La clase que proporciona las características se llama **superclase** o **clase padre**.

La clase que las recibe se llama **subclase** o **clase hija**.

En Java, la herencia entre clases se indica mediante `extends`.

```java
class Animal {
    String nombre;

    void comer() {
        System.out.println("Comiendo");
    }
}

class Perro extends Animal {
}
```

`Perro` hereda de `Animal`. Por tanto, un objeto de `Perro` puede utilizar lo que ha heredado:

```java
Perro perro = new Perro();

perro.nombre = "Max";
perro.comer();
```

La idea es establecer una relación de tipo **"es un"**:

```
Animal
   ↑
 Perro
```

Un `Perro` **es un** `Animal`, por lo que puede heredar características de `Animal`.

### ¿Para qué sirve?

La herencia permite **reutilizar código** y establecer una relación entre clases.

En lugar de volver a escribir en `Perro` todo lo que ya existe en `Animal`, `Perro` puede heredarlo y añadir sus propias características.

```java
class Perro extends Animal {
    void ladrar() {
        System.out.println("Guau");
    }
}
```

Ahora `Perro` tiene tanto lo heredado de `Animal` como su propio comportamiento.

### La herencia no significa copiar

Cuando una clase hereda de otra, no debemos entenderlo simplemente como "copiar todo el código". Se establece una **relación entre tipos**.

Esto permite que un objeto de la subclase pueda ser tratado también como un objeto de la superclase:

```java
Animal animal = new Perro();
```

Esto será especialmente importante cuando estudiemos **polimorfismo**.

### ¿Qué puede heredar?

Una subclase puede utilizar los miembros heredados que sean accesibles para ella. Los miembros `private` de la superclase **no son accesibles directamente** desde la subclase.

Además, los **constructores no se heredan**. Cuando se crea una subclase, su constructor puede utilizar `super(...)` para llamar al constructor de la superclase.

>la herencia permite que una clase especializada (`Perro`) aproveche las características de una clase más general (`Animal`) y añada o modifique su propio comportamiento.