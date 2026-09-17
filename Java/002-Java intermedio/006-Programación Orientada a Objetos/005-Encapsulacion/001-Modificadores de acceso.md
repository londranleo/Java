## Modificadores de acceso

Los **modificadores de acceso** determinan **desde dónde se puede acceder** a una clase, atributo, método o constructor.

Java tiene cuatro niveles principales de acceso:

| Modificador         | Misma clase | Mismo paquete | Subclases | Cualquier lugar |
| ------------------- | ----------- | ------------- | --------- | --------------- |
| `private`           | ✅           | ❌             | ❌         | ❌               |
| _(sin modificador)_ | ✅           | ✅             | ❌         | ❌               |
| `protected`         | ✅           | ✅             | ✅         | ❌               |
| `public`            | ✅           | ✅             | ✅         | ✅               |

### `private`

Solo permite acceder al elemento **desde la propia clase**.

```java
private int edad;
```

Se utiliza habitualmente para proteger los atributos internos de una clase.

### Acceso de paquete

Cuando no escribimos ningún modificador, el elemento puede utilizarse desde **cualquier clase del mismo paquete**.

```java
int edad;
```

También se conoce como **package-private**.

### `protected`

Permite el acceso desde la propia clase y desde clases del **mismo paquete**. Además, permite el acceso desde **subclases**, incluso si están en otro paquete, con las reglas específicas de acceso de `protected`.

```java
protected int edad;
```

### `public`

Permite acceder al elemento desde **cualquier lugar donde la clase también sea accesible**.

```java
public int getEdad() {
    return edad;
}
```

### Importante

Los modificadores de acceso no cambian el comportamiento del dato o método. Lo que cambian es **quién puede acceder a él**.

Por ejemplo, `private` no significa que el atributo sea constante ni que no pueda modificarse. Significa que **el acceso directo está restringido a la propia clase**.

>los modificadores de acceso establecen el nivel de visibilidad de los miembros de una clase. `private` restringe el acceso, `public` lo permite desde cualquier lugar accesible, y los niveles intermedios (`protected` y package-private) permiten un acceso más limitado.