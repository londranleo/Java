# Comparación

Comparar dos `String` significa comprobar si su contenido es igual. En Java existen dos formas distintas de hacerlo, y es importante no confundirlas porque no siempre dan el mismo resultado.

**El método `equals()`** compara el contenido real de los dos textos, carácter por carácter, y devuelve `true` si ambos textos son exactamente iguales, o `false` en caso contrario. Esta es la forma correcta de comparar si dos `String` representan el mismo texto.

```java
String a = "Hola";
String b = "Hola";
boolean iguales = a.equals(b);
```

**El operador `==`** no compara el contenido del texto, sino si las dos variables apuntan exactamente al mismo objeto en memoria. Dos `String` pueden tener el mismo contenido y, sin embargo, ser objetos distintos, en cuyo caso `==` devolvería `false` aunque el texto sea idéntico.

```java
String c = new String("Hola");
String d = new String("Hola");
boolean mismoObjeto = (c == d);
```

En este ejemplo, `c` y `d` contienen el mismo texto, pero al haberse creado con `new`, son dos objetos distintos en memoria, por lo que `mismoObjeto` sería `false`, mientras que `c.equals(d)` sí devolvería `true`.

Por esta razón, para comparar el contenido de dos `String` siempre debe utilizarse `equals()`, dejando `==` únicamente para los casos en los que realmente se quiere comprobar si dos variables apuntan al mismo objeto.