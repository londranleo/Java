# Reemplazar subcadenas

Reemplazar una subcadena es sustituir una parte de texto por otro dentro de una cadena. 

El métodos de `replace`  **no cambian la cadena original**, devuelven una  nueva cadena. Para conservar el resultado hay que guardarlo en una variable.  distingue entre mayúsculas y minúsculas.

- **`replace(buscado, nuevo)`**: sustituye **todas** las apariciones del texto buscado por el texto nuevo. Si el texto buscado no aparece, devuelve la cadena igual que estaba.
- **`replaceFirst(buscado, nuevo)`**: sustituye solo la **primera** aparición.

```java
String frase = "Hola mundo";

String cadenaNueva = frase.replace("mundo", "desde java");
String cadenaInicio = frase.replaceFirst("Hola", "saludos");

System.out.println(cadenaOriginal);    // Hola mundo
System.out.println(cadenaNueva);  // Hola desde java
System.out.println(cadenaInicio);    // saludos mundo
```

`replace` también funciona con un solo carácter en lugar de un texto completo:

```java
String palabra = "banana";
System.out.println(palabra.replace('a', 'o')); // bonono
```

## Eliminar texto

Para borrar una subcadena basta con reemplazarla por una cadena vacía (`""`):

```java
String codigo = "A-12-B";
System.out.println(codigo.replace("-", "")); // A12B
```
