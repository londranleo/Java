### Comparadores

Los **comparadores** permiten definir **cómo deben compararse dos objetos** cuando Java necesita determinar cuál va antes, cuál después o si ambos deben considerarse equivalentes para una determinada ordenación.

Esto es necesario especialmente cuando trabajamos con colecciones de objetos. Java puede saber cómo comparar tipos simples como números o cadenas, pero cuando tenemos una clase creada por nosotros, necesitamos definir **qué criterio utilizar para ordenar sus objetos**.

Por ejemplo, podemos decidir que una colección de personas se ordene por edad:

```java
Comparator<Persona> porEdad =
        Comparator.comparingInt(Persona::getEdad);
```

El comparador establece un criterio de orden sin tener que modificar la clase `Persona`.

Un `Comparator` utiliza el método `compare()` para determinar la relación entre dos objetos. El resultado conceptualmente indica:

```
resultado < 0  → primer objeto va antes
resultado = 0  → se consideran equivalentes según el criterio
resultado > 0  → primer objeto va después
```

Una ventaja importante es que podemos tener **diferentes criterios de ordenación para los mismos objetos**.

```
Persona
   │
   ├── ordenar por edad
   ├── ordenar por nombre
   └── ordenar por salario
```

Esto hace que `Comparator` sea muy flexible: el criterio de ordenación puede estar separado de la clase cuyos objetos estamos ordenando.

No debemos confundir `Comparator` con `Comparable`.

- **`Comparable`** → la propia clase define su orden natural.
- **`Comparator`** → define un criterio de comparación externo a la clase.

En este bloque nos interesa especialmente `Comparator` porque permite proporcionar **diferentes formas de ordenar los mismos objetos**.

> un `Comparator` define el **criterio utilizado para comparar 
> ordenar objetos**. Permite cambiar el criterio de ordenación sin 
> modificar la clase de los objetos.