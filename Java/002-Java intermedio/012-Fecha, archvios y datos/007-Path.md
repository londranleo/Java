### `Path`

`Path` es una interfaz de Java que representa **la ubicación de un archivo o directorio dentro del sistema de archivos**.

Forma parte de la API `java.nio.file`, que proporciona las herramientas modernas de Java para trabajar con archivos y directorios.

Al igual que `File`, `Path` representa una **ruta**, no el contenido del archivo.

```
Path ruta = Path.of("documentos/archivo.txt");
```

Una `Path` puede representar tanto un archivo como un directorio:

```
Path archivo = Path.of("datos.txt");
Path carpeta = Path.of("documentos");
```

Una de sus principales ventajas es que proporciona una forma más completa de **representar y manipular rutas**. Podemos obtener información sobre sus diferentes partes, resolver otras rutas, obtener su ruta absoluta o trabajar con sus componentes.

Por ejemplo:

```
Path ruta = Path.of("documentos", "archivo.txt");

Path absoluta = ruta.toAbsolutePath();
```

`Path` se utiliza normalmente junto con la clase `Files`, que proporciona las operaciones para **crear, leer, escribir, copiar, mover y eliminar** archivos y directorios.

Conceptualmente:

```
Path
 ↓
representa la ubicación
 ↓
Files
 ↓
realiza operaciones sobre esa ubicación
```

La diferencia con `File` es principalmente que `Path` pertenece a la API moderna `java.nio.file` y ofrece una representación más flexible y completa de las rutas.

```
File
→ representación tradicional de una ruta

Path
→ representación moderna de una ruta
```
