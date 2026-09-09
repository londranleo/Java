# Varargs

Los **varargs** permiten que un método reciba un **número variable de argumentos** del mismo tipo.

Se representan mediante `...` después del tipo:

```java
void mostrar(int... numeros) {
}
```

Esto permite llamar al método pasando ningún argumento, uno, o varios:

```java
mostrar();
mostrar(10);
mostrar(10, 20, 30);
```

Dentro del método, el parámetro varargs se comporta como un **array**. Por tanto, podemos acceder a sus elementos mediante índices y utilizar `length`.

```java
void mostrar(int... numeros) {
    System.out.println(numeros.length);
}
```

Un método solo puede tener **un parámetro varargs**, y este debe ser **el último parámetro** de la declaración.

```java
void ejemplo(String nombre, int... numeros) {
}
```

Esto permite combinar parámetros normales con un número variable de argumentos.

Los varargs son principalmente una **forma cómoda de pasar varios valores a un método sin tener que crear explícitamente un array**.

Internamente, los argumentos proporcionados se tratan como un array del tipo indicado.

>los varargs permiten que un método acepte una cantidad variable de argumentos. Se escriben con `...` y dentro del método se comportan como un array.