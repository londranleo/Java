## `this`

`this` es una referencia al **objeto actual**, es decir, al objeto sobre el que se está ejecutando un método o constructor.

Se utiliza principalmente para acceder a los **atributos y métodos del propio objeto**.

Por ejemplo:

```java
class Persona {
    String nombre;

    Persona(String nombre) {
        this.nombre = nombre;
    }
}
```

Aquí existen dos variables llamadas `nombre`:

- `this.nombre` → el atributo que pertenece al objeto.
- `nombre` → el parámetro del constructor.

`this` permite diferenciarlos.

### `this` en métodos

También podemos utilizar `this` para acceder explícitamente a un atributo del objeto:

```java
void mostrar() {
    System.out.println(this.nombre);
}
```

En este caso, `this.nombre` significa **el atributo `nombre` del objeto actual**.

### `this` para llamar a otro constructor

`this` también puede utilizarse para llamar a otro constructor de la misma clase:

```java
Persona() {
    this("Sin nombre");
}

Persona(String nombre) {
    this.nombre = nombre;
}
```

La llamada `this(...)` debe ser **la primera instrucción del constructor**.

Esto permite evitar repetir código entre diferentes constructores.

>`this` hace referencia al **objeto actual**. Se utiliza principalmente para acceder a sus atributos y métodos y para llamar a otro constructor de la misma clase