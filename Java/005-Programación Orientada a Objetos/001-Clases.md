## Clases

Una **clase** es una estructura que sirve para definir cómo serán los objetos de un determinado tipo.

Una clase puede contener **atributos**, que representan los datos o características del objeto, y **métodos**, que representan las acciones que puede realizar.

Por ejemplo, podemos definir una clase `Persona`:

```java
class Persona {
    String nombre;
    int edad;

    void saludar() {
        System.out.println("Hola");
    }
}
```

La clase describe qué características y comportamientos tendrá una `Persona`, pero **declarar la clase no crea una persona concreta**.

Para crear un objeto a partir de ella utilizamos `new`:

```java
Persona persona = new Persona();
```

Ahora `persona` es un **objeto**, es decir, una instancia concreta de la clase `Persona`.

Podemos tener muchos objetos creados a partir de la misma clase:

```
Clase Persona
      ↓
 ┌────┼────┐
 ↓    ↓    ↓
objeto objeto objeto
```

Cada objeto tiene su propio estado. Por ejemplo, dos objetos `Persona` pueden tener diferentes valores en `nombre` y `edad aunque pertenezcan a la misma clase.

Una clase también puede definir **constructores**, que permiten establecer el estado inicial de los objetos cuando son creados.

> una clase es la **definición o modelo** de un tipo de objeto. Define qué datos puede tener y qué operaciones puede realizar. Los objetos son las instancias concretas creadas a partir de esa clase.