## `return`

`return` se utiliza para **terminar la ejecución de un método** y, cuando corresponde, **devolver un valor** al lugar desde donde se llamó.

Si el método devuelve un valor, `return` indica qué valor debe devolver:

```java
int sumar(int a, int b) {
    return a + b;
}
```

Cuando se ejecuta `return`, el método **termina inmediatamente**. Cualquier código que aparezca después de ese `return` dentro del mismo método no se ejecutará en esa llamada.

Un método también puede utilizar `return` sin devolver un valor cuando su tipo de retorno es `void`:

```java
void mostrar() {
    return;
}
```

En este caso, simplemente termina el método.

Es importante diferenciar `return` de `break` y `continue`:

```
break     → sale del bucle o switch
continue  → salta a la siguiente iteración
return    → termina el método
```

Además, `return` puede utilizarse dentro de un bucle. En ese caso, **no solo termina el bucle**, sino que termina el método completo en el que se encuentra.

>`return` termina la ejecución del método. Si el método debe devolver un resultado, `return` proporciona ese valor al código que realizó la llamada.