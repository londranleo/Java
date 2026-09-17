### Lectura de archivos

La **lectura de archivos** consiste en obtener los datos almacenados en un archivo para que el programa pueda utilizarlos.

En la API moderna de Java, la lectura se realiza principalmente mediante la clase `Files`, utilizando un `Path` para indicar qué archivo queremos leer.

Para archivos de texto pequeños, `Files.readAllLines()` permite obtener todas las líneas del archivo:

```
Path ruta = Path.of("datos.txt");

List<String> lineas = Files.readAllLines(ruta);
```

En este caso, cada línea del archivo se almacena como un elemento de la `List`.

También podemos leer todo el contenido como un único `String`:

```
String contenido = Files.readString(ruta);
```

La elección depende de cómo necesitemos trabajar con los datos:

```
readAllLines()
→ obtiene las líneas por separado

readString()
→ obtiene todo el contenido como un String
```

Estas operaciones son apropiadas principalmente para archivos cuyo tamaño permite cargar su contenido en memoria. Para archivos grandes, existen mecanismos de lectura que permiten **procesar el contenido progresivamente**, evitando cargarlo todo de una vez.

La lectura de un archivo también puede producir errores, por ejemplo si el archivo no existe, no tenemos permisos suficientes o se produce un problema de entrada/salida. Por ello, estas operaciones pueden producir `IOException`.

```
try {
    String contenido = Files.readString(ruta);
} catch (IOException e) {
    // gestionar el error de lectura
}
```