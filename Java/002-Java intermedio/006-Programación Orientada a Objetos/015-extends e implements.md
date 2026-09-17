## `extends` e `implements`

Aunque `extends` e `implements` están relacionados con la reutilización y la abstracción, **no significan lo mismo**.

### `extends`

`extends` se utiliza cuando una clase **hereda de otra clase**.

```java
class Animal {
}

class Perro extends Animal {
}
```

`Perro` es una subclase de `Animal` y hereda los miembros accesibles de esa clase.

La relación es de tipo:

> **Perro es un Animal.**

Una clase solo puede extender directamente **una clase**.

### `implements`

`implements` se utiliza cuando una clase **implementa una interfaz**.

```java
interface Volador {
    void volar();
}

class Pajaro implements Volador {
    @Override
    public void volar() {
        System.out.println("Volando");
    }
}
```

La interfaz establece el comportamiento que `Pajaro` debe proporcionar.

Una clase puede implementar **varias interfaces**:

```java
class Pajaro implements Volador, AnimalDomestico {
}
```

### Diferencia principal

```
extends    → heredar de una clase
implements → cumplir el contrato de una interfaz
```

También pueden utilizarse juntos:

```java
class Perro extends Animal implements Mascota, Corredor {
}
```

Aquí `Perro` **hereda de `Animal`** y además **implementa dos interfaces**.

> `extends` establece una relación de herencia entre clases, mientras que `implements` establece que una clase debe cumplir los contratos definidos por una o varias interfaces.