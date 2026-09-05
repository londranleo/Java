Es una secuencia de caracteres, se utilizan para almacenar y manipular texto. 

Las cadenas son objetos de la clase `String`.

#  Índices de una cadena

Los índices en java están indexados de manera secuencial comienza desde `0` hasta longitud de la cadena. 

En el índice `N-1` siendo `N` el largo de cadena. 

# Inmutabilidad de cadenas

Una vez creada la cadena , no puede ser modificados.

Si deseamos modificar, tenemos que crear un nuevo objeto. 

# Comparación de cadenas 

`==` compara la referencia
`new String` crea un nuevo objeto.
`.equals` compara contenido.

# Métodos de cadenas

`.length()` obtener longitud.
`.replace()` remplaza caracteres.
`.toUppercase()` convierte en mayúsculas.
`.toLowercase()` convierte en minúsculas.
`.trim()` elimina espacios al inicio y final.

# Subcadenas

En general es una secuencia continua de caracteres dentro de `String`. podía ser una parte de la cadena o toda la cadena también. 

`.substring()` 

```
String nombre = "Juan";

System.out.println(nombre.substring(0,4));
System.out.println(nombre.substring(0,2));
```

**Salida**

```
Juan
Ju
```

# Bugueada subcadena 

`.indexOf()` devuelve el índice de la primera aparición.
`lastIndexOf()` devuelve la ultima aparición.

```
String nombre = "juanmanuel";
  
System.out.println(nombre.indexOf("n"));  
System.out.println(nombre.lastIndexOf("n"));
System.out.println(nombre.lastIndexOf("x"));
```

> Si la no lo encuentra devuelve `-1` 

**Salida**

```
3
6
-1
```