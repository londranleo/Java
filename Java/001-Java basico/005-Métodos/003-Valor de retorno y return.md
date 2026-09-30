## Valor de retorno y `return`

Un método puede **devolver un resultado** después de realizar su tarea. El tipo de ese resultado se indica en la declaración del método.

```java
int sumar(int a, int b) {
    return a + b;
}
```

En este caso, `int` indica que el método debe devolver un valor entero.

`return` tiene dos funciones principales:

- **Finalizar la ejecución del método.**
- **Devolver un valor**, cuando el método tiene un tipo de retorno distinto de `void`.

El valor devuelto puede almacenarse en una variable:

```java
int resultado = sumar(5, 3);
```

Aquí el método devuelve `8` y ese valor se asigna a `resultado`.

El valor que devuelve el método debe ser **compatible con el tipo de retorno declarado**. Por ejemplo, un método declarado como `int` debe devolver un valor que pueda utilizarse como `int`.

Un método `void` no necesita devolver ningún valor:

```java
void mostrar() {
    System.out.println("Hola");
}
```

En un método `void` también puede utilizarse `return` para **terminar anticipadamente el método**, pero no se puede devolver un valor.

```java
void comprobar(int numero) {
    if (numero < 0) {
        return;
    }

    System.out.println(numero);
}
```

Una vez que se ejecuta `return`, el método termina inmediatamente.

