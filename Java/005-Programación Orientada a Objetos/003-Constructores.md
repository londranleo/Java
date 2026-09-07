## Constructores

Un **constructor** es un bloque especial de una clase que se ejecuta **automáticamente cuando se crea un objeto**.

Su función principal es **inicializar el objeto**, es decir, establecer sus valores iniciales.

Tiene el mismo nombre que la clase y **no tiene tipo de retorno**, ni siquiera `void`.

```java
class Persona {
    String nombre;
    int edad;

    Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```

Al crear el objeto:

```java
Persona persona = new Persona("Leo", 22);
```

Java ejecuta automáticamente el constructor y utiliza los valores proporcionados para inicializar el objeto.

### Constructor por defecto

Si una clase **no declara ningún constructor**, Java proporciona automáticamente un constructor sin parámetros.

```java
Persona persona = new Persona();
```

Sin embargo, si declaramos nosotros mismos cualquier constructor, Java **deja de proporcionar automáticamente** ese constructor sin parámetros.

### Constructores sobrecargados

Una clase puede tener varios constructores siempre que tengan diferentes parámetros.

```java
Persona() { }

Persona(String nombre) { }

Persona(String nombre, int edad) { }
```

Esto permite crear objetos proporcionando diferentes cantidades de información inicial.

### `this`

Cuando un parámetro tiene el mismo nombre que un atributo, `this` permite hacer referencia al **atributo del objeto actual**:

```java
Persona(String nombre) {
    this.nombre = nombre;
}
```

Aquí:

- `this.nombre` → atributo del objeto.
- `nombre` → parámetro del constructor.

> el constructor se ejecuta al crear un objeto y permite establecer su estado inicial. Tiene el mismo nombre que la clase, no devuelve ningún valor y puede existir en varias versiones mediante sobrecarga.