# delete

El método `delete` elimina los caracteres comprendidos entre dos posiciones del texto: un índice inicial (incluido) y un índice final (excluido).

```java
StringBuilder sb = new StringBuilder("Java es potente");
sb.delete(4, 7);
// sb contiene: "Java potente"
```

La posición se indica mediante un índice, donde el primer carácter del texto ocupa la posición 0. Todo lo que esté entre el índice inicial y el final se elimina, y el resto del texto se desplaza hacia la izquierda para ocupar el hueco.

Al igual que otros métodos de `StringBuilder`, `delete` devuelve el propio objeto tras la modificación, por lo que permite encadenar llamadas.

```java
StringBuilder sb = new StringBuilder("Hola mundo cruel");
sb.delete(5, 11);
// sb contiene: "Hola cruel"
```