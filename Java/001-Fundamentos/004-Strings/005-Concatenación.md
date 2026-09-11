# Concatenación

La concatenación es la acción de unir dos o más textos para formar uno solo. En Java, la forma más habitual de concatenar es utilizando el operador `+` entre valores de tipo `String`.

```java
String nombre = "Ana";
String saludo = "Hola, " + nombre;
```

En este ejemplo, se une el texto `"Hola, "` con el contenido de la variable `nombre`, dando como resultado un nuevo `String` con el valor `"Hola, Ana"`.

El operador `+` también puede utilizarse para concatenar un `String` con un valor de otro tipo, como un número o un valor lógico. En ese caso, Java convierte automáticamente ese valor a su representación en texto antes de unirlo con el `String`.

```java
int edad = 25;
String texto = "Tengo " + edad + " años";
```

Como los `String` son inmutables, cada concatenación no modifica ninguno de los textos originales, sino que genera siempre un nuevo `String` con el resultado de la unión.

Cuando se encadenan varias concatenaciones seguidas en una misma expresión, Java las evalúa de izquierda a derecha, uniendo los textos en ese mismo orden.