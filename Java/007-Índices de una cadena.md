Una cadena está formada por una **secuencia ordenada de caracteres**. Cada carácter ocupa una posición determinada dentro de ella, llamada **índice**.

En Java, los índices de una cadena **comienzan siempre en `0`**. Por tanto, el primer carácter se encuentra en el índice `0`, el segundo en `1`, y así sucesivamente.

Por ejemplo, en la cadena `"Java"`:

| Indice |  0  |  1  |  2  |  3  |
| :----: | :-: | :-: | :-: | :-: |
| Cadena |  J  |  a  |  v  |  a  |

El índice de un carácter se obtiene contando desde el principio de la cadena y comenzando por `0`. La última posición siempre será **la longitud de la cadena menos uno**.

Para acceder a un carácter concreto se utiliza el método `charAt()`. Este método recibe el índice del carácter que queremos obtener y devuelve un valor de tipo `char`.

```
String lenguaje = "Java";

char caracter = lenguaje.charAt(1);
```

En este caso, `caracter` contiene `'a'`, porque `'a'` se encuentra en el índice `1`.

Los índices permiten realizar muchas operaciones sobre cadenas, como recorrer sus caracteres, buscar determinadas posiciones o trabajar con partes concretas del texto.

Es importante que el índice utilizado esté dentro de los límites de la cadena. Si se intenta acceder a una posición que no existe, Java produce una `StringIndexOutOfBoundsException`.

>**Idea clave:** un índice representa la posición de un carácter dentro de una cadena. Java
> comienza a contar desde `0`, por lo que para una cadena de longitud `n`, los índices 
> válidos van desde `0` hasta `n - 1`.