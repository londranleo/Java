## Conceptos

Los **generics** permiten crear clases, interfaces y métodos que puedan trabajar con **diferentes tipos de datos sin perder la seguridad de tipos**.

La idea principal es que podemos escribir una estructura de código de forma **genérica**, dejando que el tipo concreto se especifique cuando la utilicemos.

Por ejemplo, `List` utiliza generics:

```java
List<String> nombres;
List<Integer> edades;
```

La estructura `List` es la misma, pero el tipo de elemento cambia.

```
List<String>
→ lista de String

List<Integer>
→ lista de Integer
```

### ¿Por qué existen los generics?

Antes de los generics, muchas estructuras de Java trabajaban utilizando `Object` para poder almacenar diferentes tipos.

El problema es que entonces Java no podía comprobar de forma tan precisa qué tipo de objeto debía contener una estructura, y era necesario realizar conversiones posteriormente.

Los generics permiten indicar **qué tipo de dato puede utilizar una estructura** y hacer que el compilador compruebe que estamos utilizando correctamente ese tipo.

Por ejemplo:

```java
List<String> nombres = new ArrayList<>();

nombres.add("Leo");
nombres.add(22); // Error
```

El compilador sabe que esa lista está destinada a contener `String` y puede detectar el error antes de ejecutar el programa.

### Los tipos genéricos no son tipos concretos

Cuando escribimos:

```
List<String>
```

`String` es el **tipo concreto** que estamos proporcionando al parámetro genérico.

La `List` no está limitada a `String`. Puede trabajar con otros tipos:

```java
List<String>
List<Integer>
List<Double>
List<Persona>
```

Esto permite reutilizar la misma estructura con diferentes tipos sin tener que crear una versión diferente de `List` para cada uno.

### Concepto fundamental

Un generic puede entenderse como un **parámetro que representa un tipo**.

```
Estructura genérica
       ↓
   "¿qué tipo?"
       ↓
   tipo concreto
```

Por eso es habitual encontrar letras como:

```
T → Type
E → Element
K → Key
V → Value
```

No son palabras reservadas. Son simplemente convenciones utilizadas para representar tipos genéricos.

Por ejemplo, `Map` utiliza normalmente dos parámetros:

```
Map<K, V>
```

donde `K` representa el tipo de la clave y `V` el tipo del valor.

### Idea clave

**Los generics permiten parametrizar el código utilizando tipos**, de manera que una misma clase, interfaz o método pueda trabajar con diferentes tipos manteniendo la comprobación de tipos durante la compilación.