### `throws`

`throws` se utiliza en la **declaración de un método** para indicar que ese método puede producir o propagar determinadas excepciones.

No lanza la excepción por sí mismo. Su función es **informar al código que utiliza ese método** de que existe una excepción que puede salir del método y que, dependiendo del tipo de excepción, deberá ser gestionada.

```java
public void leerArchivo() throws IOException {
    // código
}
```

Aquí `throws IOException` significa que el método `leerArchivo()` puede terminar produciendo una `IOException`.

La excepción puede producirse dentro del método y propagarse hacia quien lo llamó:

```
método A
   ↓ llama
método B
   ↓
throws IOException
   ↓
la excepción puede subir
   ↓
método A debe gestionarla
```

Esto es especialmente importante con las **checked exceptions**, porque Java obliga a que sean gestionadas o declaradas.

Un método puede declarar varias excepciones:

```java
public void procesar() throws IOException, SQLException {
    // código
}
```

### `throw` vs `throws`

La diferencia fundamental es:

```
throw
→ lanza una excepción

throws
→ declara que un método puede lanzar una excepción
```

Por tanto:

```java
throw new IOException();
```

realiza el lanzamiento.

Mientras que:

```java
void leer() throws IOException
```

declara que el método puede propagar esa excepción.

>`throws` no lanza una excepción. **Declara en la firma de un método que determinadas excepciones pueden propagarse fuera de él**, dejando su gestión al propio método o al código que lo invoque.