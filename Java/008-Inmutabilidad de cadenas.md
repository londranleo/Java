Los objetos `String` en Java son **inmutables**. Esto significa que, una vez creado un objeto `String`, **su contenido no puede modificarse**.

Cuando realizamos una operación que parece modificar una cadena, Java no cambia el objeto original. En su lugar, se crea **otra cadena con el nuevo contenido**, y la variable puede pasar a hacer referencia a esa nueva cadena. 

Por ejemplo:

```
String nombre = "Juan";

nombre = nombre.toUpperCase();
```

En este caso, `"Juan"` no se transforma internamente en `"LEO"`. `toUpperCase()` genera una nueva cadena `"JUAN"` y posteriormente `nombre` pasa a referirse a ella.

Esto también ocurre con operaciones como `replace()`, `substring()` o la concatenación mediante `+`.

La inmutabilidad significa, por tanto, que **el contenido de un objeto `String` permanece constante durante toda su existencia**. Una variable que referencia ese objeto sí puede cambiar para referirse a otro `String`, pero el objeto original no se modifica.

Esta característica permite que Java pueda **compartir y reutilizar objetos `String` de forma segura**, como ocurre con el `_String Pool_`, ya que una cadena compartida no puede ser modificada accidentalmente por otra referencia.

También es importante diferenciar entre **modificar una cadena** y **reasignar una variable**:

```
Modificar el objeto String → no es posible
Cambiar la referencia de una variable → sí es posible
```

**Idea clave:** `String` es inmutable porque su contenido no puede cambiar después de crear el objeto. Las operaciones que producen un texto diferente crean o devuelven otra cadena; no alteran la cadena original.