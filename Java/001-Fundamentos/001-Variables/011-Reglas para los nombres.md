# Reglas para los de nombres

Las reglas para los nombres son unas reglas que casi todo el mundo sigue en Java para ponerle nombre a las cosas (variables, clases, métodos...), para que el código sea más fácil de leer por cualquier persona.

No son reglas obligatorias del lenguaje (Java no te va a dar error si no las sigues), pero es una costumbre que todos respetan para entenderse mejor entre programadores.

Estas son las más usadas:

- **Variables y métodos**: se escriben empezando en minúscula, y si el nombre tiene varias palabras, cada palabra nueva empieza en mayúscula (esto se llama *camelCase*).
```java
int edadUsuario;
void calcularTotal() { }
```

- **Clases**: se escriben empezando cada palabra en mayúscula, incluida la primera (esto se llama *PascalCase*).
```java
class CocheDeportivo { }
```

- **Constantes** (variables `final` que no cambian): se escriben todo en mayúsculas, separando las palabras con guion bajo `_`.
```java
final int EDAD_MAXIMA = 100;
```

Seguir estas costumbres no cambia cómo funciona el programa, solo ayuda a que el código se entienda mejor con un solo vistazo.