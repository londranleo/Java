## Ámbito de las variables

El **ámbito (scope)** de una variable determina **en qué parte del código se puede utilizar esa variable**.

Una variable solo puede utilizarse dentro del ámbito en el que ha sido declarada.

Por ejemplo, una variable creada dentro de un método solo existe dentro de ese método:

```java
void mostrar() {
    int numero = 10;

    System.out.println(numero);
}
```

`numero` puede utilizarse dentro de `mostrar()`, pero no fuera de él.

También ocurre con los bloques creados mediante `{}`:

```java
if (true) {
    int numero = 10;
}

System.out.println(numero); // Error
```

`numero` pertenece al bloque del `if`, por lo que deja de estar disponible cuando salimos de ese bloque.

### Variables locales

Las variables declaradas dentro de un método, constructor o bloque se denominan **variables locales**.

Su ámbito comienza donde se declaran y termina al finalizar el bloque que las contiene.

```
método
└── bloque
    └── variable local
```

Una variable declarada en un ámbito exterior puede ser utilizada desde un ámbito interior, siempre que siga siendo accesible.

```java
int numero = 10;

if (numero > 0) {
    System.out.println(numero);
}
```

El bloque `if` puede utilizar `numero` porque la variable fue declarada en un ámbito que lo contiene.

Lo contrario no ocurre: una variable creada dentro del bloque no puede utilizarse desde fuera.

### Variables con el mismo nombre

Los ámbitos también permiten que existan variables con el mismo nombre en ámbitos diferentes, aunque hacerlo puede dificultar la lectura del código.

Cuando existen variables con el mismo nombre, Java utiliza la que sea **visible dentro del ámbito actual**.

>el ámbito determina **dónde una variable existe y puede utilizarse**. Una variable local solo está disponible dentro del método o bloque donde fue declarada y dentro de los ámbitos internos que estén contenidos en él.