# ¿Qué es una variable?

Una **variable** es un espacio de memoria identificado mediante un nombre que permite **almacenar un valor durante la ejecución de un programa**.

El valor almacenado puede cambiar a lo largo de la ejecución, de ahí el nombre de variable.

# Sintaxis

```java
Tipo nombreVariable = valor;
```

- **Declaracion:** para declarar una variable se escribe primero el tipo de dato, y despues el nombre que le das 
```java
ind edad;
```

# Declaración

Declarar una variable significa indicarle a Java que vas a utilizar un espacio en la memoria del ordenador para guardar un dato, y decirle qué tipo de dato va a guardar y con qué nombre lo vas a identificar.

Para declarar una variable se escribe primero el **tipo de dato** que va a contener, y después el **nombre** que le das:

```java
int edad;
```

Es importante, indicar el tipo de dato al declarar una variable. Esto se debe a que Java es un lenguaje donde el tipo de cada dato debe quedar definido de forma clara y fija.

También puedes declarar varias variables del mismo tipo en una sola línea, separándolas por comas:

```java
int edad, altura, peso;
```


# Inicialización

Inicializar una variable significa darle un valor por primera vez después de haberla declarado. Es el momento en el que esa "caja" de memoria, que hasta entonces estaba vacía, pasa a contener realmente un dato.

La inicialización se hace utilizando el signo `=`, seguido del valor que quieres guardar:

```java
int edad = 25;
```

También es posible declarar una variable primero y darle un valor más adelante, en una línea distinta:

```java
int edad;
edad = 25;
```

Es importante inicializar una variable antes de utilizarla. Si intentas usar una variable que ha sido declarada pero nunca inicializada, Java no te dejará compilar el programa, porque no sabe qué valor tiene todavía.

Una variable puede inicializarse con un valor fijo, o con el resultado de una operación o expresión, siempre que ese resultado sea del mismo tipo que la variable:

```java
int suma = 10 + 5;
```

# Asignación

Asignar es el acto de guardar un valor dentro de una variable utilizando el signo `=`. Cada vez que usas `=` para darle un valor a una variable, estás realizando una asignación, ya sea la primera vez (inicialización) o cualquier otra vez posterior.

La diferencia es que una variable puede recibir nuevas asignaciones a lo largo del programa, no solo una vez. Como su valor puede cambiar, puedes volver a asignarle un valor distinto en cualquier momento después de que ya tenía uno:

```java
int edad = 25;
edad = 30;
```

El signo `=` en programación no significa "igual que" en el sentido matemático, sino "toma este valor y guárdalo en esta variable". Por eso se lee de derecha a izquierda: primero se calcula o se obtiene el valor de la derecha, y después ese valor se guarda en la variable de la izquierda.

Una asignación también puede usar el valor actual de la propia variable para calcular el nuevo:

```java
edad = edad + 1;
```


