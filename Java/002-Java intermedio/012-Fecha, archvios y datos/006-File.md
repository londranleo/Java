### `File`

`File` es una clase de Java que permite **representar una ruta del sistema de archivos** y trabajar con archivos y directorios.

Forma parte del paquete `java.io`.

Es importante entender que un objeto `File` **no representa el contenido de un archivo en memoria**. Representa una referencia a una ubicación del sistema de archivos.

```
File archivo = new File("documentos/archivo.txt");
```

A partir de esa referencia podemos consultar información sobre el archivo o directorio, comprobar si existe, obtener su nombre, conocer su ruta o realizar determinadas operaciones sobre él.

Por ejemplo:

```
archivo.exists();
archivo.getName();
archivo.getPath();
```

`File` puede representar tanto **archivos como directorios**.

```
File archivo = new File("datos.txt");
File carpeta = new File("documentos");
```

Una característica importante es que `File` **no se utiliza para leer o escribir directamente el contenido**. Para trabajar con los datos almacenados dentro de un archivo se utilizan otras clases de entrada y salida, como `FileReader`, `FileWriter`, `InputStream` u `OutputStream`.

Conceptualmente:

```
File
 ↓
representa una ubicación
 ↓
archivo o directorio
```

Esto permite separar el concepto de **ubicación del recurso** del concepto de **lectura o escritura de su contenido**.

Aunque `File` sigue siendo una clase válida y ampliamente conocida, Java introdujo posteriormente la API `java.nio.file`, que proporciona herramientas más modernas para trabajar con el sistema de archivos, especialmente mediante `Path` y `Files`.

```
java.io.File
→ API tradicional

java.nio.file
→ API moderna para archivos y rutas
```