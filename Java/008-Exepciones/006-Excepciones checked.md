### Excepciones checked

Las **checked exceptions** son excepciones que Java **obliga a tener en cuenta durante la compilación**.

Pertenecen a `Exception`, pero **no** a `RuntimeException`.

La característica fundamental es que, cuando un método puede producir una checked exception, el compilador exige que esa excepción sea:

- **Capturada** mediante `try-catch`.
- O **declarada** mediante `throws`.

Por ejemplo, trabajar con determinados archivos puede producir una `IOException`:

```java
public void leerArchivo() throws IOException {
    // código que puede producir IOException
}
```

En este caso, el método está declarando mediante `throws` que puede producir esa excepción.

También podríamos capturarla:

```java
try {
    leerArchivo();
} catch (IOException e) {
    // gestionar la excepción
}
```

### ¿Por qué Java las obliga?

La idea de las checked exceptions es que existen situaciones que **el programa debería prever explícitamente** porque pueden ocurrir por circunstancias externas al código.

Por ejemplo, un archivo puede no existir, una operación de entrada/salida puede fallar o una conexión con algún recurso externo puede no estar disponible.

Java intenta evitar que el programador simplemente ignore estas situaciones.

```
checked exception
       ↓
el compilador detecta que puede ocurrir
       ↓
¿Está gestionada?
   ┌───┴────┐
   ↓        ↓
  sí       no
  ↓         ↓
compila   error de compilación
```

### Checked vs unchecked

La diferencia principal es el momento en el que Java exige tratarlas:

```
Checked
→ Java obliga a gestionarlas o declararlas
→ comprobación durante compilación

Unchecked
→ Java no obliga a gestionarlas o declararlas
→ normalmente RuntimeException
```

Una checked exception no significa necesariamente que el programa vaya a fallar. Significa que **existe una situación excepcional que Java considera suficientemente previsible como para exigir que el código indique cómo la trata**.

>una checked exception es una excepción que el compilador obliga a **capturar o declarar**. Su objetivo es que determinadas situaciones previsibles, especialmente relacionadas con recursos externos, no sean ignoradas accidentalmente.