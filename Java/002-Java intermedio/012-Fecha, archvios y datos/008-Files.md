### `Files`

`Files` es una clase de Java que proporciona **métodos para realizar operaciones sobre archivos y directorios**.

Forma parte de la API `java.nio.file` y se utiliza normalmente junto con `Path`.

Mientras que `Path` representa **dónde se encuentra** un archivo o directorio, `Files` proporciona las operaciones necesarias para **trabajar con él**.

```
Path
→ representa una ubicación

Files
→ realiza operaciones sobre esa ubicación
```

Por ejemplo, podemos comprobar si una ruta existe:

```
Path ruta = Path.of("datos.txt");

Files.exists(ruta);
```

También podemos crear, copiar, mover o eliminar archivos y directorios:

```
Files.createFile(ruta);
Files.delete(ruta);
Files.copy(origen, destino);
Files.move(origen, destino);
```

`Files` también permite **leer y escribir contenido**, por lo que no necesitamos utilizar obligatoriamente las clases tradicionales de `java.io` para operaciones sencillas.

```
List<String> lineas = Files.readAllLines(ruta);

Files.write(ruta, lineas);
```

Muchas operaciones de `Files` pueden producir excepciones relacionadas con el acceso al sistema de archivos, por lo que es habitual trabajar con `IOException`.

Una característica importante es que `Files` **no representa el archivo**. Es una clase de utilidad cuyos métodos reciben normalmente un `Path` para saber sobre qué archivo o directorio deben realizar la operación.

Conceptualmente:

```
Path
  ↓
"¿Dónde está?"

Files
  ↓
"¿Qué quiero hacer con él?"
```

Por tanto, `Path` y `Files` trabajan conjuntamente y forman una parte fundamental de la API moderna de Java para el manejo del sistema de archivos.