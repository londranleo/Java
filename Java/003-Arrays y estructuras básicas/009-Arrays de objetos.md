## Arrays de objetos

Un array puede almacenar **objetos**, no solamente tipos primitivos como `int`, `double` o `boolean`.

Cuando un array almacena objetos, cada posición contiene una **referencia a un objeto**.

Por ejemplo, si tenemos una clase `Persona`:

```java
Persona[] personas = new Persona[3];
```

Esto crea un array con espacio para tres referencias a objetos `Persona`, pero **no crea las tres personas**. Inicialmente, cada posición contiene `null`.

Para que una posición contenga un objeto, debemos crear ese objeto y asignarlo:

```java
personas[0] = new Persona();
```

Ahora `personas[0]` hace referencia a una instancia de `Persona`.

Esto es importante porque un array de objetos y un array de tipos primitivos no funcionan exactamente igual:

```java
int[]       → almacena valores directamente
Persona[]   → almacena referencias a objetos
```

También podemos crear e inicializar el array directamente:

```java
Persona[] personas = {
    new Persona(),
    new Persona(),
    new Persona()
};
```

### `null`

Como las posiciones de un array de objetos contienen referencias, pueden tener el valor `null`.

`null` significa que **la referencia no apunta actualmente a ningún objeto**.

Por eso, intentar utilizar un método o atributo de una posición que contiene `null` puede provocar un `NullPointerException`.

### Acceder y modificar objetos

Al acceder a una posición obtenemos la referencia al objeto almacenado:

```java
Persona persona = personas[0];
```

Si modificamos un atributo del objeto mediante esa referencia, estamos modificando **el mismo objeto** al que apunta el array.

Esto también explica por qué, al copiar un array de objetos con métodos como `clone()` o `Arrays.copyOf()`, se crea un nuevo array pero **no se crean copias nuevas de los objetos**. Las referencias siguen apuntando a los mismos objetos.

>un array de objetos almacena referencias a objetos. Crear el array no crea automáticamente esos objetos; cada posición puede contener una referencia a un objeto o `null`.