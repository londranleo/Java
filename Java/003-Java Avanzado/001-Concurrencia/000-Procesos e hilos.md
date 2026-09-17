### Procesos e hilos

Un **proceso** es una instancia de un programa que está siendo ejecutada por el sistema operativo. Tiene su propio espacio de memoria y recursos, por lo que está aislado de otros procesos.

Un **hilo (`Thread`)** es una unidad de ejecución dentro de un proceso. Un mismo proceso puede tener varios hilos que ejecutan diferentes tareas de forma concurrente y comparten determinados recursos del proceso.

Conceptualmente:

```
Proceso
│
├── Hilo 1
├── Hilo 2
└── Hilo 3
```

La diferencia fundamental está en el nivel al que trabajan:

```
Proceso
→ programa en ejecución
→ memoria y recursos propios

Hilo
→ unidad de ejecución dentro de un proceso
→ comparte recursos del proceso
```

Los procesos están más **aislados** entre sí. Los hilos del mismo proceso, en cambio, pueden compartir memoria, lo que facilita la comunicación entre ellos pero también puede provocar problemas de concurrencia cuando varios hilos acceden simultáneamente a los mismos datos.

En Java, los hilos permiten realizar **múltiples tareas de forma concurrente**, evitando que una única tarea tenga que bloquear toda la ejecución del programa.

Por ejemplo:

```
Thread hilo = new Thread(() -> {
    System.out.println("Ejecutando en otro hilo");
});

hilo.start();
```

`start()` inicia la ejecución del hilo. No debemos confundirlo con llamar directamente al método `run()`, ya que `start()` permite que la tarea se ejecute como un hilo independiente.

También es importante distinguir **concurrencia** de **paralelismo**. La concurrencia consiste en gestionar varias tareas que pueden avanzar durante el mismo periodo, mientras que el paralelismo implica ejecutar tareas simultáneamente, normalmente utilizando varios núcleos del procesador.