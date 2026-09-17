## Setters

Un **setter** es un método que permite **modificar el valor de un atributo**, normalmente cuando ese atributo es `private`.

Por ejemplo:

```java
class Persona {
    private int edad;

    public void setEdad(int edad) {
        this.edad = edad;
    }
}
```

Como `edad` es `private`, no podemos modificarlo directamente desde otra clase:

```java
persona.edad = 22; // Error
```

En su lugar, utilizamos el setter:

```java
persona.setEdad(22);
```

El setter recibe el nuevo valor como **parámetro** y lo asigna al atributo.

### Validar antes de modificar

Una de las ventajas de utilizar setters es que la clase puede **controlar qué valores acepta**:

```java
public void setEdad(int edad) {
    if (edad >= 0) {
        this.edad = edad;
    }
}
```

Ahora:

```java
persona.setEdad(22);  // Se acepta
persona.setEdad(-5);  // No se modifica
```

De esta forma, el atributo sigue protegido y la propia clase controla cómo puede cambiarse.

### Getter y setter juntos

Es habitual utilizar ambos:

```java
class Persona {
    private String nombre;

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
}
```

```java
private atributo
      ↓
 ┌────┴────┐
 ↓         ↓
getter    setter
 ↓         ↓
leer      modificar
```

Pero **no es obligatorio tener ambos**. Podemos proporcionar solo un getter si queremos que el dato se pueda consultar pero no modificar, o solo un setter si queremos permitir su modificación sin proporcionar un método para consultarlo.

>un setter es un método que permite **modificar de forma controlada un atributo privado**. La clase puede validar el nuevo valor antes de almacenarlo.