### Wildcards

Los **wildcards** permiten trabajar con **tipos genéricos desconocidos** o con familias de tipos relacionadas mediante herencia.

Se representan con el símbolo:

```
?
```

La diferencia fundamental es que `T` representa **un tipo que conocemos o que estamos parametrizando**, mientras que `?` significa **"algún tipo, pero no sabemos exactamente cuál"**.

Por ejemplo:

```java
List<?> lista;
```

Esto significa que `lista` es una `List` de algún tipo desconocido.

Podría ser:

```
List<String>
List<Integer>
List<Persona>
```

pero el código que utiliza `List<?>` no necesita conocer cuál es exactamente ese tipo.

### ¿Para qué sirven?

Los wildcards son especialmente útiles cuando queremos que un método pueda trabajar con **colecciones genéricas de diferentes tipos** sin exigir que todas utilicen exactamente el mismo tipo.

Por ejemplo:

```java
void mostrar(List<?> lista) {
    // ...
}
```

Este método puede recibir listas de distintos tipos.

### Wildcards acotados

También podemos limitar el tipo desconocido.

Con `extends`:

```java
List<? extends Number>
```

significa que la lista contiene algún tipo que es `Number` o una clase derivada de `Number`.

```
Number
 ├── Integer
 ├── Double
 └── Float

List<? extends Number>
```

También existe `super`:

```
List<? super Integer>
```

Aquí indicamos que el tipo desconocido debe ser `Integer` o un tipo que esté **por encima de `Integer`** en la jerarquía.

Conceptualmente:

```
? extends T
→ algún tipo de T o derivado

? super T
→ algún tipo de T o superior
```

Esto permite controlar qué tipos pueden utilizarse cuando trabajamos con estructuras genéricas.

### `T` vs `?`

Esta diferencia es fundamental:

```
<T>
→ estamos definiendo/nombrando un tipo genérico

<?>
→ estamos trabajando con un tipo genérico desconocido
```

Por eso los wildcards son especialmente útiles cuando **no necesitamos conocer exactamente el tipo**, sino únicamente establecer qué tipos son aceptables.

>un wildcard (`?`) representa un **tipo genérico desconocido**. `extends` permite limitarlo hacia tipos derivados y `super` hacia tipos superiores. Los wildcards proporcionan flexibilidad al trabajar con diferentes tipos genéricos.