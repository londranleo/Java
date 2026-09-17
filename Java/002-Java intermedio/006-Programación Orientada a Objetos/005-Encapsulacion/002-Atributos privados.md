## Atributos privados

Un **atributo privado** es un atributo de una clase declarado con `private`. Esto significa que **solo puede accederse directamente desde la propia clase**.

```java
class Persona {
    private String nombre;
    private int edad;
}
```

Desde otra clase no podemos hacer:

```java
Persona persona = new Persona();

persona.edad = 22; // Error
```

El acceso directo está bloqueado porque `edad` es `private`.

### ¿Por qué hacerlos privados?

Principalmente para **proteger el estado interno del objeto**.

Si el atributo fuera público:

```java
public int edad;
```

cualquier código podría hacer:

```java
persona.edad = -500;
```

La clase no tendría control sobre el valor.

Al hacerlo privado, la clase puede decidir **cómo se consulta o modifica** ese dato:

```java
class Persona {
    private int edad;

    public void cambiarEdad(int edad) {
        if (edad >= 0) {
            this.edad = edad;
        }
    }
}
```

Ahora la modificación pasa por la propia clase:

```java
persona.cambiarEdad(22);
```

La clase puede validar el dato antes de guardarlo.

### Relación con la encapsulación

Los atributos privados son una de las herramientas principales de la **encapsulación**:

```
Objeto
│
├── datos internos
│   └── private → protegidos
│
└── métodos públicos
    └── controlan el acceso
```

Esto no significa que un atributo `private` sea necesariamente inmodificable. Significa que **otras clases no pueden acceder directamente a él**.

> un atributo privado pertenece al estado interno de la clase y solo puede ser accedido directamente desde esa misma clase. Esto permite que la clase controle cómo se utilizan y modifican sus datos.