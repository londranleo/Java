# Asignación

Asignar es el acto de guardar un valor dentro de una variable utilizando el signo `=`. Cada vez que usas `=` para darle un valor a una variable, estás realizando una asignación, ya sea la primera vez (inicialización) o cualquier otra vez posterior.

La diferencia es que una variable puede recibir nuevas asignaciones a lo largo del programa, no solo una vez. Como su valor puede cambiar, puedes volver a asignarle un valor distinto en cualquier momento después de que ya tenía uno:

```java
int edad = 25;
edad = 30;
```

Aquí la variable `edad` recibe primero el valor `25`, y más adelante se le asigna un nuevo valor, `30`, que sustituye al anterior. La variable solo puede contener un valor a la vez, así que el valor anterior se pierde en cuanto llega uno nuevo.

El signo `=` en programación no significa "igual que" en el sentido matemático, sino "toma este valor y guárdalo en esta variable". Por eso se lee de derecha a izquierda: primero se calcula o se obtiene el valor de la derecha, y después ese valor se guarda en la variable de la izquierda.

Una asignación también puede usar el valor actual de la propia variable para calcular el nuevo:

```java
edad = edad + 1;
```

En este caso, Java primero calcula el valor de `edad + 1` usando el valor que tenía en ese momento, y después guarda el resultado en `edad`, sustituyendo su valor anterior.