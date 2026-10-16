## Sobrecarga de métodos

La **sobrecarga de métodos (method overloading)** permite definir **varios métodos con el mismo nombre dentro de una clase**, siempre que tengan una **lista de parámetros diferente**.

Esto permite que una misma operación pueda utilizarse con diferentes tipos o cantidades de datos.

Por ejemplo:

```java
int sumar(int a, int b) {
    return a + b;
}

double sumar(double a, double b) {
    return a + b;
}
```

Ambos métodos se llaman `sumar`, pero reciben diferentes tipos de parámetros.

También podemos cambiar la **cantidad de parámetros**:

```java
int sumar(int a, int b) {
    return a + b;
}

int sumar(int a, int b, int c) {
    return a + b + c;
}
```

Cuando se realiza una llamada, Java determina **qué versión del método utilizar** según los argumentos proporcionados.

```java
sumar(5, 3)       → versión con 2 parámetros
sumar(5, 3, 2)    → versión con 3 parámetros
```

La diferencia entre los métodos sobrecargados debe encontrarse en sus **parámetros**: cantidad, tipos o posición de los tipos.

El **tipo de retorno por sí solo no sirve para diferenciar métodos**.

Por ejemplo, esto no sería una sobrecarga válida:

```java
int calcular(int numero) { ... }

double calcular(int numero) { ... } // Error
```

Ambos tienen exactamente los mismos parámetros, aunque sus tipos de retorno sean diferentes.

La sobrecarga se resuelve **en tiempo de compilación**, porque Java determina qué método corresponde según la información disponible en la llamada.

> la sobrecarga permite tener varios métodos con el mismo nombre siempre que sus parámetros sean diferentes. Así podemos utilizar el mismo nombre para una operación que funciona con diferentes tipos o cantidades de datos.