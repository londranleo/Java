# Lifetime (tiempo de vida)

El "lifetime" de algo en Java es el tiempo que esa cosa existe en la memoria del ordenador, desde que se crea hasta que desaparece.

Por ejemplo, una variable que declaras dentro de un método solo existe mientras ese método se está ejecutando. En cuanto el método termina, esa variable desaparece de la memoria, como si se borrara.

En cambio, un objeto que creas con `new` puede durar más tiempo. Sigue existiendo en la memoria mientras algo lo esté usando (por ejemplo, mientras una variable siga apuntando a él). Cuando ya nadie lo usa, Java lo elimina automáticamente para liberar espacio.

```java
void metodo() {
    int numero = 5; // el lifetime de "numero" dura solo mientras se ejecuta este método
}
```

Así que el lifetime responde a una pregunta muy simple: ¿durante cuánto tiempo existe esto en la memoria antes de desaparecer?