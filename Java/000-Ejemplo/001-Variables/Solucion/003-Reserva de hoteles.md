[[Java/000-Ejemplo/001-Variables/Reto/003-Reserva de hoteles|003-Reserva de hoteles]]

```java
public class ReservaDeHoteles {  
  
    public static void main(String[] args) {  
  
        // Detalle reserva  
        String nombreCilente = "Juan Gomez";  
        int diasEstancia = 5;  
        double precioDia = 69.99;  
        boolean tieneVistaAlMar = true;  
  
        //Imprime por consola  
        System.out.println("nombreCilente = " + nombreCilente);  
        System.out.println("diasEstancia = " + diasEstancia);  
        System.out.println("precioDia = " + precioDia);  
        System.out.println("tieneVistaAlMar = " + tieneVistaAlMar);  
  
        //Modifica valores  
        diasEstancia = 4;  
        tieneVistaAlMar = false;  
  
        //Imprime valores modificados  
        System.out.println("nombreCilente = " + nombreCilente);  
        System.out.println("diasEstancia = " + diasEstancia);  
        System.out.println("precioDia = " + precioDia);  
        System.out.println("tieneVistaAlMar = " + tieneVistaAlMar);  
  
    }  
}
```

**Salida** 

```java
nombreCilente = Juan Gomez
diasEstancia = 5
precioDia = 69.99
tieneVistaAlMar = true

nombreCilente = Juan Gomez
diasEstancia = 4
precioDia = 69.99
tieneVistaAlMar = false
```