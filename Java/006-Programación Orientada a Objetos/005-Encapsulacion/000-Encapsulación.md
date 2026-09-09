## Encapsulación

La **encapsulación** consiste en **controlar cómo se puede acceder y modificar el estado interno de un objeto**.

Una clase normalmente no debería permitir que cualquier parte del programa pueda modificar directamente sus datos sin ningún control. Para conseguirlo, podemos restringir el acceso a sus atributos y proporcionar métodos para trabajar con ellos.

Por ejemplo:

```java
class Persona {
    private int edad;

    public void setEdad(int edad) {
        if (edad >= 0) {
            this.edad = edad;
        }
    }

    public int getEdad() {
        return edad;
    }
}
```

Aquí `edad` es `private`, por lo que no se puede modificar directamente desde fuera de la clase.

En lugar de hacer:

```java
persona.edad = -10;
```

se utiliza el método:

```java
persona.setEdad(-10);
```

El método puede decidir si el valor es válido antes de modificar el atributo.

La encapsulación no significa simplemente **poner los atributos como `private`**. La idea es que la propia clase controle cómo se accede a su estado y qué operaciones se pueden realizar sobre él.

Los modificadores de acceso (`private`, `public`, `protected` y el acceso de paquete) permiten establecer quién puede acceder a los miembros de una clase.

>la encapsulación permite proteger el estado interno de un objeto y controlar cómo otras partes del programa pueden acceder o modificarlo.