### Tipos acotados

Los **tipos acotados** permiten limitar qué tipos pueden utilizarse como parámetro genérico.

Normalmente, cuando utilizamos un generic como `T`, puede representar prácticamente cualquier tipo:

```
T → cualquier tipo permitido
```

Con un tipo acotado podemos decir que `T` **debe pertenecer a una determinada clase o jerarquía**.

Por ejemplo:

```java
<T extends Number>
```

Esto significa que `T` debe ser `Number` o una clase que herede de `Number`.

```
Number
   │
   ├── Integer
   ├── Double
   └── Float
```

Por tanto, estos tipos serían válidos:

```java
<T extends Number>
```

con:

```
Integer
Double
Float
```

pero un tipo que no pertenezca a esa jerarquía no sería válido.

### ¿Para qué sirven?

La utilidad principal es que podemos **restringir el tipo y, al mismo tiempo, indicarle al compilador qué características puede asumir que tiene ese tipo**.

Por ejemplo, si sabemos que `T` siempre será algún tipo de `Number`, podemos utilizar operaciones y métodos proporcionados por `Number` dentro del código genérico.

Sin la restricción:

```
<T>
```

el compilador no puede asumir que `T` tenga las características de una clase concreta.

Con la restricción:

```
<T extends Number>
```

sí puede asumir que `T` pertenece a esa jerarquía.

### También pueden utilizar interfaces

La palabra `extends` se utiliza tanto para clases como para interfaces en los tipos genéricos.

```
<T extends Comparable<T>>
```

Esto significa que el tipo utilizado debe implementar `Comparable<T>`.

De esta manera, el método genérico puede trabajar sabiendo que el tipo proporciona el comportamiento definido por esa interfaz.

### La idea fundamental

Un generic sin restricción:

```
<T>
```

permite un conjunto muy amplio de tipos.

Un generic acotado:

```
<T extends Algo>
```

reduce ese conjunto y establece una **condición que el tipo debe cumplir**.

>los tipos acotados permiten **restringir los tipos que pueden utilizarse en un generic**. Esto proporciona más seguridad y permite que el código genérico trabaje con las características garantizadas por la clase o interfaz utilizada como límite.