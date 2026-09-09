## Objetos e instancias
Un **objeto** es una entidad creada a partir de una clase. Contiene sus propios **datos** y puede utilizar los **métodos definidos por su clase**.

Una **instancia** es simplemente un objeto que ha sido creado a partir de una determinada clase. Por tanto, cuando decimos que un objeto es una instancia de una clase, estamos indicando **de qué clase ha sido creado**.

```java
Persona persona = new Persona();
```

Aquí:

- `Persona` → tipo de la variable.
- `persona` → referencia que utilizamos para acceder al objeto.
- `new Persona()` → crea una nueva instancia de `Persona`.

Podemos crear varias instancias de una misma clase:

```java
Persona persona1 = new Persona();
Persona persona2 = new Persona();
```

`persona1` y `persona2` son **dos objetos diferentes**, aunque ambos pertenecen a la clase `Persona`.

Cada instancia tiene su propio estado. Si una persona tiene un atributo `edad`, cambiar la edad de `persona1` no cambia automáticamente la edad de `persona2`.

Es importante distinguir entre **objeto y referencia**. La variable `persona` no contiene directamente el objeto, sino una **referencia al objeto** creado en memoria.

```
persona ───────→ objeto Persona
```

También podemos tener varias referencias que apunten al mismo objeto:

```java
Persona persona1 = new Persona();
Persona persona2 = persona1;
```

Ahora no existen dos objetos. Existen **dos referencias al mismo objeto**.

```
persona1 ──┐
           ├──→ objeto Persona
persona2 ──┘
```

Por eso, modificar el objeto utilizando cualquiera de las dos referencias afecta al mismo objeto.

>una clase define cómo es un tipo de objeto, mientras que una instancia es un objeto concreto creado a partir de esa clase. Las variables de tipo objeto almacenan referencias que permiten acceder a esas instancias.