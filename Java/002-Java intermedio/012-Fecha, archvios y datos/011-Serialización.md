### Serialización

La **serialización** es el proceso de convertir el **estado de un objeto** en una representación que pueda **almacenarse o transmitirse** y posteriormente utilizarse para reconstruir el objeto.

La idea principal es pasar de un objeto que existe en memoria a una representación que pueda guardarse, por ejemplo, en un archivo.

```
Objeto en memoria
       ↓
  Serialización
       ↓
Representación de datos
       ↓
Archivo / transmisión
```

En Java, la serialización tradicional se realiza mediante la interfaz `Serializable`.

```
class Persona implements Serializable {
    private String nombre;
    private int edad;
}
```

Al implementar `Serializable`, la clase indica que sus objetos pueden participar en el mecanismo de serialización de Java.

El proceso inverso se denomina **deserialización**. Consiste en reconstruir un objeto a partir de la representación que había sido almacenada o transmitida.

```
Datos almacenados
       ↓
Deserialización
       ↓
Objeto en memoria
```

La serialización puede utilizarse para **persistir temporalmente el estado de objetos** o transmitirlos entre procesos, aunque en aplicaciones modernas existen alternativas como JSON, XML u otros formatos, especialmente cuando los datos necesitan ser intercambiados entre sistemas diferentes.

Una característica importante de la serialización tradicional de Java es que no se guarda simplemente el código de la clase, sino **el estado serializable del objeto** necesario para reconstruirlo.

Los atributos marcados como `transient` quedan excluidos de la serialización:

```
private transient String contraseña;
```

Esto permite indicar que determinado estado no debe formar parte de la representación serializada.