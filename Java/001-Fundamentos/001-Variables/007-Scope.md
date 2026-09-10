# Scope

El scope es el lugar donde una variable puede usarse.

En Java, una variable solo se puede usar dentro del bloque de código donde la creaste (lo que está entre `{ }`).

```java
void metodo() {
    int numero = 10;
    // aquí sí se puede usar
}
// aquí ya no se puede usar
```

Cuando ese bloque termina, la variable desaparece. Por eso puedes tener dos variables con el mismo nombre en partes distintas del código, sin que se molesten entre sí: cada una existe en su propio bloque.