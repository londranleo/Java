El tipo de dato `var` fue introducido en Java 10 con el objetivo de inferir de datos en variable locales (variable definidas dentro de un metodo).

Permite declarar una variable sin especificar explícitamente su tipo. El tipo se determina automáticamente a partir del valor que se asigna a la variable cuando se declara, haciendo que el codigo sea mas conciso y legible.

```java                     
//Ejemplo sin usar var
int edad = 22;
String nombre = "Juan";
double precio = 19.99;
```

```java
//ejemplo con var 
var edad = 22;
var nombre = "Juan";
var precio = 19.99;
```

# Reglas de var 

- El uso var es exclusivo para definir variables locales dentro de metodo. No puede ser usado para definir variables de clases o parametros de metodos. 

- Debe se inicializada al declararse, en la misma linea donde se declara

```java
var numero; //error la variable debe ser inicializada
numero = 10;
```

- El tipo debe ser inferible.

```java
var lista = null; //error no se puede interir el tipo
```



