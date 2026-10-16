```java
import java.util.Locale;  
  
public class GeneradorDeEmail {  
  
  
    public static void main(String[] args) {  
  
  
        String nombre = " Ana Lopez Soto ";  
        String empresas = " Java Interprice " ;  
        String dominio = ".com.es";  
  
        String nombreLimpio = nombre.toLowerCase();  
        String eliminaEspaciopIF = nombreLimpio.trim();  
        String puntos = eliminaEspaciopIF.replace(" ", ".");  
  
  
        String empresaLimpio = empresas.toLowerCase();  
        String eliminaE = empresaLimpio.trim();  
        String puntos1 = eliminaE.replace(" ", ".");  
  
  
        System.out.println(puntos + "@" + puntos1 + dominio);  
  
  
    }  
}
```