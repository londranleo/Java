# Conversión `String`

En Java es habitual necesitar convertir valores entre el tipo `String` (texto) y otros tipos de datos, como los números. Esta conversión no sigue las mismas reglas que la conversión entre tipos numéricos, porque un texto y un número son conceptos completamente distintos: no basta con cambiar cómo se interpreta el valor, sino que hay que transformarlo de verdad.

**De número a texto** es una conversión sencilla, ya que cualquier número puede representarse siempre como texto. Se puede hacer concatenando el número con una cadena vacía:

```java
int edad = 25;
String texto = "" + edad;
```

**De texto a número** es más delicada, porque no todo texto representa un número válido. Para hacerlo, se utilizan métodos específicos proporcionados por las clases envoltorio de cada tipo numérico, como `Integer.parseInt()` para convertir a `int` o `Double.parseDouble()` para convertir a `double`:

```java
String texto = "42";
int numero = Integer.parseInt(texto);
```

Si el texto no tiene el formato de un número válido (por ejemplo, contiene letras), este proceso lanzará un error en tiempo de ejecución, ya que Java no puede completar la conversión.