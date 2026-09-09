## `super`

`super` es una palabra clave que permite acceder a **elementos de la superclase desde una subclase**.

Se utiliza principalmente para:

- Acceder a un atributo de la superclase.
- Llamar a un método de la superclase.
- Llamar al constructor de la superclase.

### Acceder a un método de la superclase

Si una subclase sobrescribe un método heredado, `super` permite ejecutar la versión de la superclase:

```java
class Animal {
    void hacerSonido() {
        System.out.println("Sonido");
    }
}

class Perro extends Animal {
    @Override
    void hacerSonido() {
        super.hacerSonido();
        System.out.println("Guau");
    }
}
```

`super.hacerSonido()` hace referencia específicamente al método definido en `Animal`.

### Acceder a un atributo

También podemos utilizar `super` para referirnos al atributo heredado cuando existe otro atributo con el mismo nombre en la subclase:

```java
class Animal {
    String nombre = "Animal";
}

class Perro extends Animal {
    String nombre = "Perro";

    void mostrar() {
        System.out.println(super.nombre);
    }
}
```

Aquí `super.nombre` hace referencia al `nombre` de `Animal`, mientras que `this.nombre` haría referencia al `nombre` de `Perro`.

### Llamar al constructor de la superclase

`super(...)` permite llamar a un constructor de la superclase:

```java
class Animal {
    Animal(String nombre) {
        System.out.println(nombre);
    }
}

class Perro extends Animal {
    Perro(String nombre) {
        super(nombre);
    }
}
```

La llamada a `super(...)` dentro de un constructor debe ser **la primera instrucción**.

Si no escribimos explícitamente una llamada a `super(...)`, Java intenta llamar automáticamente al **constructor sin parámetros** de la superclase. Si este no existe, el constructor de la subclase debe llamar explícitamente a uno disponible.

> `super` permite que una subclase acceda explícitamente a la parte heredada de la superclase. Con `super(...)` llamamos a su constructor; con `super.método()` a su método y con `super.atributo` a su atributo.