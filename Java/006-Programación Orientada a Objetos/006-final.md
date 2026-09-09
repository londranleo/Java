## `final`

El siguiente tema es **`final`**, que se utiliza para indicar que algo **no puede cambiarse después de haber sido definido**.

### Variable `final`

Una variable `final` solo puede recibir un valor **una vez**.

```java
final int EDAD = 22;
```

Después de asignarle un valor, no podemos reasignarla:

```java
EDAD = 30; // Error
```

Esto hace que una variable `final` sea una **constante** cuando representa un valor que debe mantenerse fijo.

### Atributos `final`

Un atributo también puede ser `final`:

```java
class Persona {
    final String DNI;
}
```

Una vez inicializado, ese atributo no puede recibir otro valor.

### Método `final`

Un método `final` **no puede sobrescribirse** en una subclase.

Esto será importante cuando estudiemos herencia.

```java
final void mostrar() {
    System.out.println("Hola");
}
```

Una clase que herede de esta clase no podrá proporcionar otra implementación de `mostrar()`.

### Clase `final`

Una clase `final` **no puede ser heredada**:

```java
final class Persona {
}
```

No se puede crear una clase que extienda `Persona`.

### Idea clave

`final` significa, en general, **"esto no puede modificarse de esta manera después de establecerlo"**:

```java
variable final → no se puede reasignar
método final   → no se puede sobrescribir
clase final   → no se puede heredar
```

>**Importante:** `final` no significa que un objeto sea completamente inmutable. Si una variable `final` contiene una referencia a un objeto, la referencia no puede cambiar, pero el estado interno del objeto puede ser modificable.