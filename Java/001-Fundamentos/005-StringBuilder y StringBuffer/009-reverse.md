# reverse

El método `reverse` invierte el orden de todos los caracteres del texto actual, modificando el mismo objeto.

```java
StringBuilder sb = new StringBuilder("Java");
sb.reverse();
// sb contiene: "avaJ"
```

No recibe ningún parámetro: simplemente recorre el texto y coloca los caracteres en orden inverso. Al igual que otros métodos de `StringBuilder`, devuelve el propio objeto tras la modificación, por lo que permite encadenar llamadas junto a otros métodos.

```java
StringBuilder sb = new StringBuilder("Hola");
sb.reverse().append("!");
// sb contiene: "aloH!"
```