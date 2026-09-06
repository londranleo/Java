Una **constante** es un valor que, una vez establecido, **no puede ser reasignado durante la ejecución del programa**. Se utiliza cuando un valor debe mantenerse fijo y no debe cambiar accidentalmente.

En Java, las constantes se crean utilizando la palabra clave `final`. Al declarar una variable como `final`, solo puede recibir una asignación válida una vez.

```
final int EDAD_MAXIMA = 18;
```

Después de asignarle un valor, no se puede realizar otra asignación:

```
EDAD_MAXIMA = 21; // Error
```

`final` no hace que el valor sea necesariamente conocido durante la compilación; simplemente impide **reasignar la variable** después de que haya sido inicializada.

Una variable `final` debe recibir un valor antes de utilizarse. La asignación puede realizarse directamente al declararla o posteriormente, siempre que solo se realice una vez.

Las constantes se utilizan para representar valores que tienen un significado fijo dentro del programa, como límites, cantidades o valores matemáticos. Evitan repetir valores directamente en diferentes partes del código y permiten modificar ese valor desde un único lugar cuando sea necesario.

Por convención, cuando una constante es `static final`, su nombre se escribe utilizando **mayúsculas y guiones bajos**:

```
static final double IVA = 0.21;
```

`static` y `final` tienen funciones diferentes: `static` hace que el miembro pertenezca a la clase en lugar de a cada objeto, mientras que `final` impide que la variable sea reasignada.

### Importante

`final` impide cambiar **la referencia o el valor almacenado en la variable**, pero no significa necesariamente que el objeto al que apunta sea inmutable.

Por ejemplo, una referencia `final` a un objeto no puede apuntar a otro objeto, pero el estado interno de ese objeto podría seguir siendo modificable. Esta diferencia será especialmente importante cuando estudiemos **objetos, referencias e inmutabilidad**.