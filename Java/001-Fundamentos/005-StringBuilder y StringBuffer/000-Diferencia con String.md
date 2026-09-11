# Diferencia con String

En Java, un `String` es **inmutable**: una vez creado, su contenido no puede cambiar. Cada vez que se modifica un `String` (por ejemplo, concatenando texto), en realidad no se cambia el objeto original, sino que se crea uno completamente nuevo en memoria, y el anterior queda descartado.

```java
String texto = "Hola";
texto = texto + " mundo";
// No se modifica "Hola", se crea un nuevo String "Hola mundo"
```

Esto no supone ningún problema si el texto se modifica pocas veces. Sin embargo, si se realizan muchas modificaciones seguidas (por ejemplo, dentro de un bucle), se van creando muchos objetos `String` innecesarios uno tras otro, y los anteriores quedan descartados en memoria a la espera de ser eliminados. Esto afecta al rendimiento del programa, ya que crear y descartar objetos constantemente tiene un coste.

`StringBuilder` y `StringBuffer` existen precisamente para evitar este problema: permiten modificar el contenido del texto directamente sobre el mismo objeto, sin necesidad de crear uno nuevo cada vez que se realiza un cambio.