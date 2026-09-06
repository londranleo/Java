Una **subcadena** es una parte de una cadena de caracteres que se obtiene a partir de una sección determinada de otra cadena. Permite trabajar únicamente con una parte del texto original sin tener que utilizar la cadena completa.

En Java, las subcadenas se obtienen principalmente mediante el método `substring()`. Este método utiliza los **índices de la cadena** para determinar desde qué posición comienza y hasta qué posición se obtiene el texto.

`substring()` puede utilizarse de dos formas:

- Indicando únicamente el índice inicial: obtiene los caracteres desde esa posición **hasta el final de la cadena**.
- Indicando un índice inicial y uno final: obtiene los caracteres desde el inicio indicado **hasta antes del índice final**.

Esto último es importante: **el índice inicial se incluye, pero el índice final no**.

Por ejemplo:

```
String texto = "Programacion";

String parte = texto.substring(0, 6);
```

El resultado es:

```
"Progra"
```

Los índices `0` a `5` se incluyen, mientras que el índice `6` queda fuera.

La subcadena obtenida es un **nuevo `String`** y, debido a la inmutabilidad de las cadenas, la cadena original no se modifica.

También hay que tener en cuenta que los índices utilizados deben encontrarse dentro de los límites permitidos. Si se proporciona una posición no válida, Java produce una excepción.

>**Idea clave:** `substring()` permite extraer una parte concreta de una cadena utilizando sus índices. El inicio se incluye y el final se excluye, y la operación no modifica la cadena original.