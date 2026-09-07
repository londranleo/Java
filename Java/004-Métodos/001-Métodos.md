## Métodos

Un **método** es un bloque de código que contiene una serie de instrucciones destinadas a realizar una **tarea concreta**.

Los métodos permiten dividir un programa en partes más pequeñas y reutilizables. En lugar de escribir las mismas instrucciones cada vez que necesitamos realizar una operación, podemos definirlas una vez dentro de un método y llamarlo cuando sea necesario.

La estructura general es:

```java
tipoRetorno nombreMetodo(parámetros) {
    // instrucciones
}
```

Por ejemplo:

```java
int sumar(int a, int b) {
    return a + b;
}
```

Aquí:

- `int` → indica el tipo de valor que devuelve.
- `sumar` → nombre del método.
- `int a, int b` → parámetros que necesita.
- `return` → devuelve el resultado.

Para ejecutar un método debemos **invocarlo**:

```
int resultado = sumar(5, 3);
```

Los valores `5` y `3` son los **argumentos** que se proporcionan al método.

### Métodos que no devuelven un valor

Un método puede realizar una acción sin devolver ningún resultado. Para ello se utiliza `void`.

```
void mostrarMensaje() {
    System.out.println("Hola");
}
```

En este caso el método realiza una acción, pero no devuelve un valor.

### Parámetros y argumentos

Es importante diferenciar ambos conceptos:

- **Parámetro** → variable que se declara en la definición del método.
- **Argumento** → valor que proporcionamos cuando llamamos al método.

```java
int sumar(int a, int b) {
    return a + b;
}
```

`a` y `b` son parámetros.

```java
sumar(5, 3);
```

`5` y `3` son argumentos.

### Métodos y ámbito

Las variables declaradas dentro de un método pertenecen a su **ámbito local**. Solo pueden utilizarse dentro de la zona donde han sido declaradas.

Esto permite que diferentes métodos tengan sus propias variables sin interferir directamente entre sí.

### Métodos como unidades reutilizables

Un método puede utilizarse varias veces y cada llamada puede recibir valores diferentes.

Esto permite evitar duplicación de código y separar las distintas responsabilidades de un programa.

>un método es un bloque de código que realiza una tarea concreta. Puede recibir datos mediante parámetros y puede devolver un resultado mediante `return`, o no devolver ninguno utilizando `void`.