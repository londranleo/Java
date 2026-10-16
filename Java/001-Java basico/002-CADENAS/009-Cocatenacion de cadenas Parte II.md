# El método `concat`

`concat` es un método de `String` que une otra cadena al final de la cadena sobre la que se llama. Como las cadenas no se pueden modificar, no cambia ninguna de las dos: **devuelve una cadena nueva**.

```java
String a = "Ho";
String b = "La";

String c = a.concat(b);

System.out.println(c); // Hola 
```

Solo acepta cadenas: no se le puede pasar  un número ni otro tipo de valor. Si se le pasa `null`, el programa lanza una excepción (`NullPointerException`). Si la cadena que se añade está vacía (`""`), devuelve la misma cadena original.

# StringBuilder

`StringBuilder` es una clase para construir textos que **sí se pueden modificar**. A diferencia de `String`, que crea una cadena nueva con cada cambio, un `StringBuilder` guarda el texto en un mismo objeto y lo va cambiando por dentro. Esto lo hace mucho más eficiente cuando hay que unir muchos trozos de texto, por ejemplo dentro de un bucle, donde usar `+` crearía una cadena nueva en cada vuelta.

Se crea con `new`, y cuando el texto está terminado se obtiene como `String` con `toString()`.

```java
StringBuilder sb = new StringBuilder("Hola");

sb.append(" mundo");       // añade al final
sb.append("!");
sb.insert(0, ">> ");       // inserta en la posición 0
sb.reverse();              // da la vuelta al texto

String resultado = sb.toString();
System.out.println(resultado); // !odnum aloH >>
```

Métodos habituales:

- **`append(valor)`**: añade al final. Acepta texto, números y otros valores, convirtiéndolos a texto.
- **`insert(posición, valor)`**: inserta en la posición indicada.
- **`delete(inicio, fin)`**: borra desde `inicio` hasta justo antes de `fin`.
- **`replace(inicio, fin, texto)`**: sustituye ese tramo por el texto indicado.
- **`reverse()`**: invierte el orden de los caracteres.
- **`length()`**: devuelve la cantidad de caracteres.


```java
String texto = new StringBuilder()
        .append("uno")
        .append(", ")
        .append("dos")
        .toString();

System.out.println(texto); // uno, dos
```

# StringBuffer

`StringBuffer` funciona prácticamente igual que `StringBuilder`: texto modificable, con los mismos métodos (`append`, `insert`, `delete`, `replace`, `reverse`, `toString`...).

```java
StringBuffer sb = new StringBuffer("Hola");
sb.append(" mundo");

System.out.println(sb); // Hola mundo
```

La diferencia es que `StringBuffer` está **sincronizado**: sus métodos están protegidos para que, si varias partes del programa lo usan a la vez, el texto no se corrompa. Esa protección tiene un coste en velocidad, por lo que `StringBuilder`, al no tenerla, es más rápido. En la práctica se usa `StringBuilder` salvo que se necesite esa protección.

# El método `join`

`String.join` une varios textos en una sola cadena, colocando entre ellos un **separador** que se elige. Es un método estático: se llama sobre la clase `String`, no sobre una cadena concreta. El separador solo aparece **entre** los elementos, nunca al principio ni al final.

```java
String resultado = String.join("-", "2026", "10", "02");

System.out.println(resultado); // 2026-10-02
```

El primer parámetro es el separador y el resto son los textos a unir (puede haber los que se quieran). El separador puede ser cualquier cadena, incluso una vacía o un espacio:

```java
System.out.println(String.join(" ", "Hola", "mundo")); // Hola mundo
System.out.println(String.join("", "ca", "sa"));       // casa
```

También puede recibir una colección de textos ya preparada en lugar de elementos sueltos, y la une del mismo modo.

