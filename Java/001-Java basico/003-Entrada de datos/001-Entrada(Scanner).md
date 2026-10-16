# Entrada

Para recibir datos desde la consola podemos utilizar `Scanner`, Pertenece al paquete `java.util`

```java
import java.util.Scanner;

public class LeerLinea {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		String nombre = sc.nextLine();
	}
}
```

`System.in` representa la **entrada estándar**, normalmente el teclado cuando ejecutamos el programa desde una consola.

`Scanner` permite interpretar los datos recibidos según el tipo que necesitemos:

| Metodo          | Tipo de dato |
| --------------- | ------------ |
| `nextLine()`    | String       |
| `nextInt()`     | int          |
| `nextDouble()`  | double       |
| `nextBoolean()` | boolean      |

La entrada no tiene por qué proceder únicamente del teclado. Un programa también puede recibir datos desde **archivos, redes, bases de datos, interfaces gráficas u otras fuentes**. En este apartado nos centramos en la entrada básica por consola.

