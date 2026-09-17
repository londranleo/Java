### `Runnable`

`Runnable` es una **interfaz funcional** que representa una tarea que puede ser ejecutada por un hilo.

A diferencia de `Thread`, `Runnable` **no representa el hilo en sí**. Representa únicamente **el trabajo que queremos que se ejecute**.

```
Runnable
→ representa la tarea

Thread
→ representa el hilo que ejecuta la tarea
```

`Runnable` tiene un único método abstracto, `run()`, que define el código que debe ejecutarse.

```
Runnable tarea = () -> {
    System.out.println("Ejecutando tarea");
};
```

Después podemos proporcionar esa tarea a un `Thread`:

```
Thread hilo = new Thread(tarea);

hilo.start();
```

De esta forma separamos **la tarea que queremos realizar** del **mecanismo utilizado para ejecutarla**.

También podemos utilizar directamente una expresión lambda porque `Runnable` es una interfaz funcional:

```
Thread hilo = new Thread(() -> {
    System.out.println("Ejecutando tarea");
});

hilo.start();
```

`Runnable` no devuelve ningún resultado. Su método `run()` tiene retorno `void`.

```
Runnable
   ↓
run()
   ↓
ejecuta una tarea
   ↓
sin valor de retorno
```

Esta separación es importante porque una misma tarea `Runnable` puede ser ejecutada por diferentes mecanismos. Por ejemplo, puede entregarse a un `Thread` o posteriormente a un **`ExecutorService`**, que permite gestionar la ejecución de tareas mediante un conjunto de hilos.