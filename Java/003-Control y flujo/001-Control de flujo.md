# Control de flujo

El **control de flujo** es la forma en la que Java decide **qué código ejecutar y cuándo ejecutarlo**.

Normalmente, Java ejecuta las instrucciones **de arriba hacia abajo**, siguiendo el orden en el que están escritas.

```java
System.out.println("Primero");
System.out.println("Segundo");
System.out.println("Tercero");
```

Se ejecutan en ese mismo orden.

El control de flujo permite cambiar este comportamiento. Por ejemplo, podemos hacer que:

- Un código se ejecute **solo si se cumple una condición**.
    
- Se elija entre **diferentes opciones**.
    
- Un código se repita **varias veces**.
	
- Una repetición se detenga o pase a la siguiente vuelta.
    

Para conseguirlo, Java proporciona diferentes estructuras:

- `if` / `else` → tomar decisiones.
	
- `switch` → elegir entre varias opciones.
    
- `while`, `do-while` y `for` → repetir código.
    
- `break` → salir de una estructura.
    
- `continue` → pasar a la siguiente repetición.
    
- `return` → salir de un método.
    

Por ejemplo:

```java
if (edad >= 18) {
    System.out.println("Puedes entrar");
}
```

Aquí Java **comprueba una condición** y solo ejecuta el código si se cumple.

>El control de flujo permite decidir **qué instrucciones se ejecutan, cuáles no y cuáles se repiten**.