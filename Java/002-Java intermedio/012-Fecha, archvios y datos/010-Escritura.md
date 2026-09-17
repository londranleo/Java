### Escritura de archivos

La **escritura de archivos** consiste en almacenar información desde el programa dentro de un archivo del sistema de archivos.

En la API moderna de Java, la escritura se realiza principalmente mediante la clase `Files`, utilizando un `Path` para indicar dónde queremos guardar la información.

Para escribir texto en un archivo podemos utilizar `Files.writeString()`:

```
Path ruta = Path.of("datos.txt");

Files.writeString(ruta, "Hola mundo");
```

También podemos escribir una colección de líneas mediante `Files.write()`:

```
List<String> lineas = List.of(
    "Primera línea",
    "Segunda línea"
);

Files.write(ruta, lineas);
```

Por defecto, estas operaciones **crean el archivo si no existe** y, cuando el archivo ya existe, pueden reemplazar su contenido dependiendo de las opciones utilizadas.

Java permite especificar diferentes **opciones de escritura** para controlar el comportamiento, como añadir información al final del archivo en lugar de reemplazar su contenido.

```
Files.writeString(
    ruta,
    "Nueva línea\n",
    StandardOpenOption.APPEND
);
```

Conceptualmente:

```
Programa
   ↓
Files.write(...)
   ↓
Path
   ↓
archivo
   ↓
datos almacenados
```

Al igual que ocurre con la lectura, las operaciones de escritura pueden producir `IOException`, por ejemplo si no tenemos permisos para escribir en la ubicación indicada.

```
try {
    Files.writeString(ruta, "Hola mundo");
} catch (IOException e) {
    // gestionar el error de escritura
}
```