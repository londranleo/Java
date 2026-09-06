Los **caracteres especiales** son caracteres que tienen un significado particular dentro de una cadena o que permiten representar elementos que no se pueden escribir directamente de la forma habitual.

En Java, algunos caracteres tienen un significado especial cuando aparecen dentro de un `String`. Para indicar que queremos utilizar ese carácter con su significado literal o representar determinados caracteres especiales, se utilizan **secuencias de escape**.

Una secuencia de escape comienza normalmente con una **barra invertida** `**\**`, seguida de otro carácter que determina qué se quiere representar.

Los más utilizados son:

|Secuencia|Significado|
|---|---|
|`\n`|Salto de línea|
|`\t`|Tabulación|
|`\"`|Comillas dobles|
|`\'`|Comilla simple|
|`\\`|Barra invertida|
|`\r`|Retorno de carro|
|`\b`|Retroceso|
|`\f`|Salto de página|

Por ejemplo, las comillas dobles normalmente indican el comienzo y el final de un `String`. Si queremos incluir unas comillas dentro del propio texto, debemos escaparlas:

```
String mensaje = "Él dijo: \"Hola\"";
```

El resultado contiene las comillas como parte del texto:

```
Él dijo: "Hola"
```

También podemos utilizar caracteres de escape para controlar el formato del texto:

```
String texto = "Hola\nMundo";
```

Aquí `\n` representa un salto de línea, por lo que el texto se muestra en dos líneas.

Es importante entender que una secuencia como `\n` **se escribe utilizando dos caracteres en el código (**`\` **y** `n`**), pero representa un carácter especial dentro de la cadena**.

Los caracteres especiales son especialmente útiles cuando necesitamos representar **saltos de línea, tabulaciones, comillas, barras invertidas u otros caracteres cuyo significado normal entra en conflicto con la sintaxis de Java**.

>**Idea clave:** las secuencias de escape permiten representar caracteres o comportamientos especiales dentro de una cadena utilizando una combinación que comienza con `\`.