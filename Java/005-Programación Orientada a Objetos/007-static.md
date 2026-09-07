## `static`

`static` indica que un atributo o método **pertenece a la clase y no a cada objeto**.

Normalmente, cuando creamos un objeto, cada objeto tiene sus propios atributos:

```java
Persona p1 = new Persona();
Persona p2 = new Persona();
```

Si `nombre` es un atributo normal, `p1` y `p2` tienen cada uno su propio `nombre`.

Con `static`, en cambio, existe **una única variable asociada a la clase**, compartida por todos sus objetos.

```java
class Persona {
    static int contador;
}
```

`contador` pertenece a `Persona`, no a una persona concreta.

Por eso podemos acceder a él mediante la propia clase:

```java
Persona.contador
```

### Métodos `static`

Un método también puede ser `static`:

```java
class Calculadora {
    static int sumar(int a, int b) {
        return a + b;
    }
}
```

Como pertenece a la clase, podemos llamarlo sin crear un objeto:

```java
int resultado = Calculadora.sumar(5, 3);
```

### ¿Qué implica `static`?

La diferencia fundamental es:

```java
Sin static → pertenece a cada objeto
Con static → pertenece a la clase
```

Un método `static` no está asociado a un objeto concreto. Por eso **no puede acceder directamente a los atributos o métodos de instancia**, ya que estos necesitan un objeto específico.

```java
class Persona {
    String nombre;

    static void mostrar() {
        // System.out.println(nombre); // Error
    }
}
```

Para acceder a `nombre`, sería necesario disponer de una instancia concreta.

`static` se utiliza habitualmente para **datos compartidos**, métodos que no necesitan el estado de un objeto y miembros que conceptualmente pertenecen a la clase.

> `static` hace que un miembro pertenezca a la **clase en lugar de a las instancias**. Los miembros `static` pueden utilizarse sin crear un objeto de esa clase.