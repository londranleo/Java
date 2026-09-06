la palabra clave `var`  permite declarar una variable sin especificar explícitamente su tipo. El tipo se determina automáticamente a partir del valor que se asigna a la variable cuando se declara.

```
var edad = 22;
var nombre = "Juan";
var precio = 19.99;
```

En cada caso, el tipo se obtiene del valor inicial:
- `edad` → `int`
- `nombre` → `String`
- `precio`  → `double`
Una vez determinado el tipo, la variable se comporta como cualquier otra variable de ese tipo. `var` no representa un tipo especial ni permite que la variable cambie de tipo posteriormente. 

Por ejemplo, si `edad` se ha determinado como `int`, solo podrá recibir valores compatibles con `int`:

```
edad = 25; → correcto    
edad = "vente" → error
```

La inferencia del tipo ocurre al **compilar el código**. El compilador analiza la expresión utilizada para inicializar la variable y determina qué tipo debe tener. Por esta razón, `var` necesita que exista un valor inicial del que pueda obtenerse el tipo.

No se debe interpretar `var` como "una variable cuyo tipo no conocemos". El tipo sí existe y está determinado; simplemente **no lo escribimos nosotros porque el compilador puede deducirlo**.

`var` se utiliza principalmente cuando el tipo puede deducirse fácilmente del valor o de la expresión inicial. Su utilidad está en evitar escribir tipos que resultan evidentes, manteniendo el comportamiento y las comprobaciones propias del tipo determinado.

Ejemplo conceptual

```
var numero = 10;
```

Es equivalente, respecto al tipo de la variable, a:

```
int numero = 10;
```

La diferencia es que con `var` dejamos que el compilador determine que `numero` debe ser `int`.