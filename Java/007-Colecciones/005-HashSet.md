## `HashSet`

`HashSet` es una **implementación de `Set`** que permite almacenar elementos **sin duplicados**.

```java
Set<String> nombres = new HashSet<>();
```

La característica principal de `HashSet` es que utiliza una estructura basada en **hashing** para localizar los elementos.

### Añadir elementos

```java
nombres.add("Ana");
nombres.add("Luis");
nombres.add("Carlos");
nombres.add("Ana");
```

El segundo `"Ana"` no se añade porque ya existe.

```java
Ana
Luis
Carlos
```

### No utiliza índices

No podemos hacer:

```java
nombres.get(0); // Error
```

Para recorrer los elementos:

```java
for (String nombre : nombres) {
    System.out.println(nombre);
}
```

### El orden no está garantizado

Una característica importante de `HashSet` es que **no garantiza el orden en el que se recorren los elementos**.

Por ejemplo, aunque hagamos:

```java
nombres.add("Ana");
nombres.add("Luis");
nombres.add("Carlos");
```

no debemos asumir que al recorrerlo obtendremos:

```java
Ana
Luis
Carlos
```

El orden puede ser diferente.

Por eso, si necesitas una colección que mantenga un orden concreto, `HashSet` no es la opción adecuada.

### Comprobar si existe un elemento

Podemos utilizar `contains()`:

```java
if (nombres.contains("Ana")) {
    System.out.println("Ana existe");
}
```

También podemos eliminar elementos:

```java
nombres.remove("Ana");
```

Y conocer la cantidad de elementos:

```java
int cantidad = nombres.size();
```

### ¿Por qué no hay duplicados?

Para determinar si un elemento ya existe, `HashSet` utiliza principalmente **`hashCode()` y `equals()`**.

Esto se vuelve especialmente importante cuando almacenamos **objetos propios**:

```java
Set<Persona> personas = new HashSet<>();
```

En ese caso, debemos entender cómo funcionan `equals()` y `hashCode()` para definir correctamente cuándo dos objetos deben considerarse iguales.

Eso lo veremos cuando lleguemos a objetos y colecciones.

### Idea clave

`HashSet` es una implementación de `Set` que:

```java
HashSet
│
├── No permite duplicados
├── No utiliza índices
├── No garantiza el orden
├── add()       → añadir
├── remove()    → eliminar
├── contains()  → comprobar existencia
└── size()      → obtener cantidad
```

>`HashSet` está pensado principalmente para trabajar con **elementos únicos** y realizar operaciones de búsqueda, inserción y eliminación de forma eficiente, sin depender de una posición concreta.