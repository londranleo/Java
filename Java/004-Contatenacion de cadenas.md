La concatenación de cadenas consiste en unir dos o mas cadenas de texto para formar una nueva cadena. En java, la forma mas habitual de realizarla es mediante el operador `+`.

Cuando se utiliza `+` con valores de tipo `String`, java interpreta la operación como una concatenación en lugar de una suma. El resultado es una **nueva cadena** que contiene los caracteres de los valores concatenados en el mismo orden.

```
String nombre = "Juan";
String saludo = "Hola ";
```

**Salida** de `saludo` será:

```
Hola Juan 
```

La concatenación también puede combinar cadena con valores de otros tipos. Cuando uno de los operandos es un `String`, el otro valor se convierte en una representación textual y ambos se concatenan.

```
int edad 22;
String mensaje = "Tengo " + edad + " anios"
```

**Salida** de `mensaje` será:

```
Tengo 22 anios
```

Es importante distinguir la concatenación de la suma. El operador `+` puede realizar ambas operaciones dependiendo de los tipos de los operandos. Con números realiza una operación aritmética; cuando interviene un `String`, se utiliza para concatenar.

Además, las operaciones de concatenación con `String` no modifican las cadenas originales, ya que `String` es inmutable. El resultado de la concatenación es una **nueva cadena**.

### Orden de evaluación

Cuando existen varias operaciones con `+`, Java las evalúa de izquierda a derecha, teniendo en cuenta los tipos presentes en cada momento.

Por eso, la posición de los valores puede cambiar completamente el resultado:

```
System.out.println(10 + 20 + " Java");
System.out.println("Java " + 10 + 20);
```

El primer caso comienza realizando una suma numérica antes de encontrar el `String`, mientras que en el segundo la presencia inicial del `String` hace que los valores siguientes se concatenen como texto.

**Idea clave:** `+` no significa siempre suma. Su comportamiento depende de los tipos de los operandos: **entre números suma; cuando interviene un `String`, concatena**.

### `Metodo Concat()`

`concat()` es un método de `String` destinado específicamente a unir una cadena con otra.

```
String resultado = "Hola ".concat("Leo");
```

A diferencia de `+`, `concat()` recibe una cadena como argumento y devuelve un nuevo `String` con ambas cadenas unidas. Como `String` es inmutable, tampoco modifica ninguna de las cadenas originales.

Su uso es sencillo, aunque en la mayoría de situaciones el operador `+` resulta más cómodo y legible.

### `StringBuilder`

`StringBuilder` está diseñado para **construir y modificar texto de forma progresiva**. A diferencia de `String`, su contenido es mutable, por lo que puede añadir, eliminar o modificar caracteres sin tener que crear un nuevo `String` después de cada operación.

Esto resulta especialmente útil cuando se realizan muchas concatenaciones, por ejemplo, al construir texto dentro de un bucle.

```
StringBuilder texto = new StringBuilder();
texto.append("Hola ");
texto.append("Leo");
```

Cuando se termina de construir el contenido, se puede obtener un `String` mediante `toString()`.

Su principal ventaja frente a concatenar repetidamente mediante `String` es que está pensado específicamente para trabajar con modificaciones sucesivas del contenido.

### `StringBuffer`

`StringBuffer` tiene una función similar a `StringBuilder`: permite construir y modificar una secuencia de caracteres de manera mutable.

La principal diferencia está relacionada con la **concurrencia**. `StringBuffer` proporciona operaciones sincronizadas, lo que permite utilizarlo de forma segura en determinados escenarios donde varios hilos pueden acceder al mismo objeto.

Esta sincronización introduce una sobrecarga adicional. Por ello, cuando no es necesaria la sincronización, normalmente se prefiere `StringBuilder`.

### `String.join()`

`String.join()` está pensado especialmente para **unir varios elementos utilizando un separador**.

Por ejemplo, resulta útil para crear una cadena a partir de varios valores separados por una coma, un espacio, un guion u otro delimitador.

```
String resultado = String.join(", ", "Java", "Python", "C++");
```

El resultado será:

```
Java, Python, C++
```

A diferencia de las formas anteriores, `join()` resulta especialmente útil cuando existe una colección o secuencia de elementos que queremos convertir en una única cadena utilizando un separador común.

### ¿Cuál utilizar?

La elección depende de la situación:

- `+` → concatenaciones sencillas y expresiones pequeñas.
- `concat()` → unión directa de una cadena con otra.
- `StringBuilder` → construcción progresiva de texto y muchas concatenaciones.
- `StringBuffer` → construcción progresiva de texto cuando se necesita sincronización entre hilos.
- `String.join()` → unir varios elementos utilizando un separador.

Todas estas operaciones tienen como objetivo producir texto combinado, pero **no funcionan exactamente de la misma manera ni están pensadas para los mismos escenarios**.

>**Idea clave:** para concatenaciones simples, `+` suele ser la opción más clara. Para construir texto mediante muchas modificaciones se utiliza `StringBuilder`, mientras que `StringBuffer` añade sincronización para escenarios concurrentes. `String.join()` está orientado a unir múltiples elementos mediante un separador.