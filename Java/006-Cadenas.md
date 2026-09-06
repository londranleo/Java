Una **cadena de caracteres** es una secuencia de caracteres utilizada para representar texto. En Java, las cadenas se representan mediante la clase `String`.

A diferencia de los tipos primitivos como `int`, `double` o `boolean`, `String` es un **tipo de referencia**, ya que representa objetos.

Una cadena puede contener cualquier cantidad de caracteres, incluyendo una cadena vacía. Los caracteres que forman la cadena mantienen un orden determinado y cada uno ocupa una posición dentro de ella. Estas posiciones permiten acceder posteriormente a caracteres concretos o trabajar con partes de la cadena.

Las cadenas se representan mediante comillas dobles. El contenido situado entre ellas forma parte del valor de la cadena.

```
String nombre = "Juan";
```

En este caso, `nombre` hace referencia a un objeto `String` cuyo contenido es `"Juan"`.

Una característica fundamental de `String` es que sus objetos son **inmutables**. Esto significa que, una vez creado un objeto `String`, su contenido no puede modificarse directamente. Las operaciones que parecen modificar una cadena producen en realidad otra cadena con el nuevo contenido.

Las cadenas proporcionan numerosos métodos para trabajar con su contenido, como obtener su longitud, acceder a caracteres, comparar cadenas, buscar texto o extraer subcadenas.

También es posible combinar cadenas con otros valores mediante la **concatenación**, utilizando normalmente el operador `+`.

```
String nombre = "Leo";
String mensaje = "Hola " + nombre;
```

El resultado es una nueva cadena formada por la unión de los valores.

**Idea clave:** `String` representa texto mediante una secuencia ordenada de caracteres y proporciona operaciones para consultar y trabajar con ese contenido. Al ser inmutable, las operaciones que generan un contenido diferente producen una nueva cadena en lugar de modificar la original.
