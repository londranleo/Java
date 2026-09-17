## Sobreescritura de métodos (`@Override`)

La **sobrescritura (overriding)** ocurre cuando una subclase proporciona **su propia implementación de un método que ya existe en la superclase**.

La idea es que la clase hija pueda cambiar el comportamiento heredado para adaptarlo a sus necesidades.

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
```

`Perro` hereda `hacerSonido()` de `Animal`, pero lo **sobrescribe** proporcionando una nueva implementación.

Al hacer:

```java
Perro perro = new Perro();
perro.hacerSonido();
```

se ejecuta la versión de `Perro`.

### `@Override`

`@Override` es una **anotación** que indica que el método está sobrescribiendo un método heredado.

No es obligatorio escribirla para que la sobrescritura funcione, pero es muy recomendable porque permite que el compilador compruebe que realmente estamos sobrescribiendo un método existente.

### Reglas principales

Para sobrescribir un método:

- Debe existir un método heredado con el que coincida la firma.
- No se puede reducir su nivel de acceso.
- El tipo de retorno debe ser compatible.
- Un método `final` no puede sobrescribirse.
- Los métodos `private` no se sobrescriben porque no son heredados por la subclase.

> la sobrescritura permite que una subclase **cambie la implementación de un método heredado** para proporcionar un comportamiento específico.