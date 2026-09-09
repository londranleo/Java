## `List`

`List` es una **interfaz de Java** que representa una colección de elementos que se mantienen en un **orden determinado** y a los que podemos acceder mediante su **posición (índice)**.

A diferencia de un array, una `List` puede **cambiar de tamaño** durante la ejecución del programa.

```java
List<String> nombres = new ArrayList<>();
```

Aquí `List` indica **qué comportamiento queremos** y `ArrayList` es la implementación que lo proporciona.

Podemos añadir elementos:

```java
nombres.add("Ana");
nombres.add("Luis");
nombres.add("Carlos");
```

La lista mantiene el orden en el que fueron añadidos:

```java
índice    0       1        2
          ↓       ↓        ↓
        Ana     Luis    Carlos
```

Podemos acceder a un elemento mediante su índice:

```java
String nombre = nombres.get(1);
```

El resultado sería `"Luis"`.

También podemos modificar o eliminar elementos:

```java
nombres.set(1, "Pedro");
nombres.remove(0);
```

### Características principales

Una `List`:

- Mantiene el **orden** de los elementos.
- Permite acceder mediante **índices**.
- Permite elementos **duplicados**.
- Puede aumentar o disminuir su tamaño.
- No es una clase concreta, sino una **interfaz**.

Por ejemplo:

```java
List<String> nombres = new ArrayList<>();
```

La variable es de tipo `List`, pero el objeto creado es un `ArrayList`.

Esto permite programar utilizando el **tipo general (`List`)** en lugar de depender de una implementación concreta.

```java
List
  │
  ├── ArrayList
  └── LinkedList
```

Tanto `ArrayList` como `LinkedList` implementan `List`, por lo que ambas pueden utilizarse cuando necesitamos una lista, aunque internamente funcionan de manera diferente.

>`List` representa una colección ordenada y accesible por índice que permite duplicados y cuyo tamaño puede cambiar. `ArrayList` y `LinkedList` son implementaciones de `List`.