[[Java/000-Ejemplo/001-Variables/Reto/002-Detalle de un producto de una tienda Linea|002-Detalle de un producto de una tienda Linea]]

```java
public class TiendaEnLinea {  
  
    public static void main(String[] args) {  
  
        //Detalle producto  
        System.out.println("---Tienda en linea---");  
        String nombreProducto = "laptop HP";  
        double precio = 199.69;  
        int cantidad = 32;  
        boolean disponible = true;  
  
        //Imprime por consola  
		System.out.println("nombreProducto = " + nombreProducto);  
        System.out.println("precio = " + precio);  
        System.out.println("cantidad = " + cantidad);  
        System.out.println("disponible = " + disponible);  
  
        //Modifica los valores  
        nombreProducto = "laptop HP pro";  
        precio = 300.00;  
        cantidad = 0;  
        disponible = false;  
  
        //imprime valores modificados  
        System.out.println("nombreProducto = " + nombreProducto);  
        System.out.println("precio = " + precio);  
        System.out.println("cantidad = " + cantidad);  
        System.out.println("disponible = " + disponible);  
  
    }  
}
```

**Salida**

```text
---Tienda en linea---
nombreProducto = laptop HP
precio = 199.69
cantidad = 32
disponible = true
nombreProducto = laptop HP pro
precio = 300.0
cantidad = 0
disponible = false
```