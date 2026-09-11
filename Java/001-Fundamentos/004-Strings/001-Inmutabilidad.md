# Inmutabilidad

La inmutabilidad es una característica de `String` que significa que, una vez creado un texto, su contenido no puede cambiarse ni modificarse de ninguna forma durante la ejecución del programa.

Cuando se realiza una operación que parece modificar un `String` —como concatenarlo con otro texto o convertirlo a mayúsculas—, en realidad Java no altera el texto original, sino que crea un **nuevo** objeto `String` con el resultado de esa operación, dejando el original exactamente igual que antes.

```java
String texto = "Hola";
texto = texto + " mundo";
```

En este ejemplo, el `String` original `"Hola"` no se modifica; se crea un nuevo `String` con el contenido `"Hola mundo"`, y la variable `texto` pasa a apuntar a ese nuevo objeto en lugar del anterior.

Esta característica existe porque los textos se usan con mucha frecuencia en un programa, y al ser inmutables, Java puede reutilizar y compartir de forma segura el mismo `String` en distintas partes del código sin riesgo de que una parte del programa modifique accidentalmente un texto que otra parte también está utilizando.

Como consecuencia práctica, cualquier método de `String` que "modifica" un texto en realidad siempre devuelve un `String` nuevo, y ese resultado debe guardarse (normalmente reasignándolo a una variable) si se quiere conservar el cambio.