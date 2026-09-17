### `throw`

`throw` se utiliza para **lanzar una excepción de forma explícita** desde el código.

Hasta ahora hemos visto que una excepción puede producirse cuando Java encuentra una situación problemática durante la ejecución. Con `throw`, somos nosotros quienes indicamos directamente que **debe producirse una excepción**.

Su finalidad principal es comunicar que una determinada situación **no es válida o no puede continuar normalmente**.

```java
throw new IllegalArgumentException("La edad no puede ser negativa");
```

En este caso, el programa crea una excepción de tipo `IllegalArgumentException` y la lanza.

Cuando se ejecuta `throw`, el flujo normal del método **se interrumpe inmediatamente** y Java busca un `catch` compatible para gestionar la excepción.

Conceptualmente:

```
código
  ↓
throw
  ↓
se lanza una excepción
  ↓
se interrumpe el flujo normal
  ↓
catch compatible
```

`throw` es especialmente útil para **validar condiciones**. La propia aplicación puede detectar que un dato no cumple las reglas esperadas y lanzar una excepción.

Por ejemplo:

```
if (edad < 0) {
    throw new IllegalArgumentException("Edad inválida");
}
```

### `throw` vs `throws`

Es importante no confundirlos:

```
throw
→ lanza una excepción concreta

throws
→ declara que un método puede lanzar determinadas excepciones
```

`throw` se utiliza **dentro del código** para realizar el lanzamiento.

`throws` se utiliza en la **declaración del método** para informar de las excepciones que puede propagar.

>`throw` permite que el propio programa **lance explícitamente una excepción** cuando detecta una situación que debe considerarse excepcional.