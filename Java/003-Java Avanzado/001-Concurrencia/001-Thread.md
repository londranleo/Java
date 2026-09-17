### `Thread`

`Thread` es una **clase de Java que representa un hilo de ejecución**. Permite ejecutar una tarea de manera independiente dentro de un proceso.

Un programa puede tener varios `Thread` ejecutándose de forma concurrente, permitiendo que diferentes tareas avancen durante el mismo periodo de ejecución.

```
Thread hilo = new Thread(() -> {
    System.out.println("Tarea ejecutándose");
});

hilo.start();
```

Al llamar a `start()`, Java inicia el hilo y ejecuta la tarea definida en él.

Un `Thread` tiene su propio **flujo de ejecución**, pero comparte con los demás hilos del mismo proceso recursos como la memoria del proceso.

```
Proceso
│
├── Thread 1
│
├── Thread 2
│
└── Thread 3
```

Cada hilo puede encontrarse en diferentes **estados durante su ciclo de vida**, como nuevo, ejecutable, bloqueado, esperando o terminado. Estos estados reflejan la situación en la que se encuentra el hilo respecto a su ejecución.

Una característica importante es que crear y gestionar muchos `Thread` directamente puede resultar costoso y complicado. En aplicaciones reales, normalmente se utilizan mecanismos de nivel superior, como **`ExecutorService`**, para gestionar grupos de hilos y distribuir tareas.

También es importante distinguir entre `start()` y `run()`:

```
hilo.start(); // inicia un nuevo hilo
hilo.run();   // ejecuta run() en el hilo actual
```

Llamar directamente a `run()` **no crea un nuevo hilo**.