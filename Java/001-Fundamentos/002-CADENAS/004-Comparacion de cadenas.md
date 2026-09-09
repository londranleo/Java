La comparación de cadenas cosiste en determinar si dos objetos `String` son iguales, diferentes o, en algunos casos, cual aparece antes o después que otro.

En java es importante distinguir entre **comparar el contenido de las cadenas y comparar las referencias que apuntan a ellas**.

Para comparar el codecido de dos cadenas se utiliza principalmente el método `equals()`. Este método comprueba si ambas cadenas contiene la misma secuencia de caracteres.

```
String nombre1 = "Juan";
String nombre2 = "Juan";

nombre1.equals(nombre2); //true
```

El operador `==`, en cambio, no esta pensado para comprobar si dos `String` tiene el mismo contenido. Al utilizarlo con objetos, compara sus referencias, es decir, comprueba si ambas variables hacen referencia al mismo objeto.

Por ejemplo:

```
String a = new String("Java");
String b = new String("Java");

a == b;  //false
a.equals(b)  //true
```

Aunque amabas cadenas contienen `Java`, Son objetos diferentes. por eso `==` devuelve `false`, mientras que `equals()` devuelve `true`.

Esta diferencia es especialmente importante debido a que Java puede reutilizar determinadas cadenas mediante el **String Pool**. Dos variables pueden terminar haciendo referencia al mismo objeto aunque esto no sea algo que debamos utilizar para comparar el contenido de las cadenas.

También existe `equalsIgnoreCase()`, que permite comparar el contenido ignorando las diferencias entre mayúsculas y minúsculas.

```
"Java" y "JAVA"
```

se consideran iguales utilizando `equalsIgnoreCase()`.

Además de comprobar igualdad, Java proporciona `compareTo()` para realizar una **comparación lexicográfica**, es decir, comparar las cadenas según el orden de sus caracteres. El resultado permite saber si una cadena es menor, igual o mayor que otra según ese orden.

> **Idea clave:** para comparar el contenido de dos `String` se utiliza `equals()`. `==` compara referencias, no el contenido. Esta diferencia es fundamental al trabajar con objetos en Java.
