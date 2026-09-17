## Getters

Un **getter** es un método que permite **obtener o consultar el valor de un atributo**, normalmente cuando ese atributo es `private`.

Por ejemplo:

```java
class Persona {
    private String nombre;

    public String getNombre() {
        return nombre;
    }
}
```

Como `nombre` es `private`, otra clase no puede acceder directamente:

```java
persona.nombre; // Error
```

Pero puede obtener su valor mediante el getter:

```java
String nombre = persona.getNombre();
```

El getter normalmente:

1. Es `public`.
2. Devuelve el mismo tipo que el atributo.
3. No recibe parámetros.
4. Utiliza `return` para devolver el valor.

```java
public int getEdad() {
    return edad;
}
```

Aquí `getEdad()` permite **leer** el valor de `edad`, pero no modificarlo.

Esto forma parte de la encapsulación:

```java
private atributo
      ↓
   getter
      ↓
 consultar el valor
```

Es importante entender que el getter **no es obligatorio** para todos los atributos privados. La clase decide qué información quiere permitir consultar. Un atributo puede ser `private` y no tener getter si no queremos que otras clases puedan obtener su valor directamente.

>un getter es un método que proporciona acceso controlado para **consultar el valor de un atributo privado**, sin exponer directamente el atributo.