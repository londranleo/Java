## Agregación

La **agregación** es una relación entre dos clases en la que un objeto **tiene o utiliza otro objeto**, pero ambos pueden **existir de forma independiente**.

Por ejemplo, una `Universidad` puede tener `Estudiantes`:

```java
class Estudiante {
    String nombre;
}

class Universidad {
    private Estudiante estudiante;

    Universidad(Estudiante estudiante) {
        this.estudiante = estudiante;
    }
}
```

Podemos crear primero el estudiante:

```java
Estudiante estudiante = new Estudiante();
Universidad universidad = new Universidad(estudiante);
```

Aquí `Universidad` utiliza al objeto `Estudiante`, pero el estudiante **no depende de la universidad para existir**.

```java
Universidad
     │
     └── tiene → Estudiante
                    ↑
              puede existir
              por separado
```

### Agregación vs composición

La diferencia importante está en la **dependencia entre los objetos**:

```java
Agregación
Universidad ───→ Estudiante
                  ↓
            puede existir
            independientemente


Composición
Coche ─────────→ Motor
                   ↓
             forma parte del
             coche
```

En la composición, normalmente el objeto contenido forma parte del ciclo de vida del objeto que lo contiene. En la agregación, los objetos tienen una relación más independiente.

>la agregación representa una relación **"tiene un"** en la que el objeto contenido puede existir independientemente del objeto que lo utiliza.