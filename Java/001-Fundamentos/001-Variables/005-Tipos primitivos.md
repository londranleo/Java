# Tipos primitivos

Los tipos primitivos son los tipos de datos más básicos que ofrece Java para almacenar valores simples, como números, caracteres o valores verdadero/falso. Se llaman "primitivos" porque no están construidos a partir de otras estructuras más complejas: son el nivel más fundamental con el que Java representa la información.

Cuando declaras una variable con un tipo primitivo, el valor se guarda directamente en la memoria, ocupando un espacio fijo y conocido de antemano según el tipo. Esto los hace muy eficientes en cuanto a rendimiento y uso de memoria, ya que Java no necesita gestionar nada adicional aparte del propio valor.

Java define un conjunto cerrado de ocho tipos primitivos, cada uno pensado para representar una clase concreta de dato: números enteros, números con decimales, un único carácter o un valor verdadero/falso. Cada tipo primitivo tiene su propio tamaño y rango de valores que puede almacenar.

Los tipos primitivos se diferencian de los llamados **tipos de referencia** (como los objetos) en que una variable primitiva contiene el valor en sí misma, mientras que una variable de referencia contiene, en realidad, la dirección de memoria donde está guardado el valor.

```java
int numero = 10;
```

En este ejemplo, `numero` es una variable de tipo primitivo que guarda directamente el valor `10`, sin ninguna capa adicional entre la variable y el dato.