## Parámetros y argumentos

Los **parámetros** y los **argumentos** son la forma en la que un método puede **recibir información desde el código que lo llama**.

### Parámetros

Los **parámetros** son las variables que se declaran en la definición del método. Representan los datos que el método espera recibir.

```java
int sumar(int a, int b) {
    return a + b;
}
```

En este caso, `a` y `b` son parámetros.

Los parámetros actúan como **variables locales del método** y reciben un valor cada vez que el método es invocado.

### Argumentos

Los **argumentos** son los valores que proporcionamos al llamar al método.

```java
sumar(10, 5);
```

Aquí `10` y `5` son los argumentos que se asignan a `a` y `b`.

La relación es:

```java
Parámetro → variable definida por el método
Argumento → valor proporcionado al llamar al método
```

El número y los tipos de los argumentos deben ser compatibles con los parámetros definidos por el método.

Por ejemplo, si un método espera dos `int`, la llamada debe proporcionar valores que puedan utilizarse como esos parámetros.

### Paso de argumentos

En Java, los argumentos se pasan a los métodos **por valor**.

Esto significa que el método recibe una copia del valor de la variable utilizada como argumento.

Con tipos primitivos, modificar el parámetro dentro del método **no modifica la variable original**.

Con objetos, el valor que se copia es la **referencia al objeto**. Por ello, el método puede modificar el estado del objeto al que apunta esa referencia, pero reasignar el parámetro para que apunte a otro objeto no cambia la referencia original.

Este comportamiento es importante porque Java **no utiliza paso por referencia de variables**.

>los parámetros son las variables que un método declara para recibir información y los argumentos son los valores que se proporcionan al realizar la llamada. En Java, los argumentos siempre se pasan por valor.