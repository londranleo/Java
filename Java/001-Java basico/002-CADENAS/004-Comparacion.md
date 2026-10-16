La comparación de cadenas cosiste en determinar si dos objetos `String` son iguales o diferentes.

En java es importante distinguir entre **comparar el contenido de las cadenas y comparar las referencias que apuntan a ellas**.

Para comparar el contenido de dos cadenas se utiliza principalmente el método `equals()`. Este método comprueba si ambas cadenas contiene la misma secuencia de caracteres.

```java
String cadena1 = "Java";
String cadena2 = "Java";

nombre1.equals(nombre2); //true
```

Para comparar la referecia se usa El operador `==`, comprueba si ambas variables hacen referencia al mismo objeto.

```java
String a = new String("Java");
String b = new String("Java");

a == b;  //false
a.equals(b)  //true
```

Aunque amabas cadenas contienen `Java`, Son objetos diferentes. por eso `==` devuelve `false`, mientras que `equals()` devuelve `true`.

También existe `equalsIgnoreCase()`, que permite comparar el contenido ignorando las diferencias entre mayúsculas y minúsculas.

```java
String cadena1 = "Java";
String cadena2 = "JAVA";
```

se consideran iguales utilizando `equalsIgnoreCase()`.



