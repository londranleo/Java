# Casting

El **casting** es el nombre general que recibe la acción de indicar explícitamente que un valor debe tratarse como si fuera de otro tipo, escribiendo el tipo deseado entre paréntesis delante del valor:

```text
(tipoDestino) valor
```

Aunque ya se ha visto aplicado a tipos numéricos, el casting también se utiliza con **objetos**, es decir, con variables cuyo tipo es una clase. En este caso, el casting no cambia el objeto en sí, sino que le indica a Java cómo debe tratarlo en ese momento.

Existen dos direcciones posibles al hacer casting entre objetos relacionados:

- **De un tipo más específico a uno más general**: Java lo permite de forma automática, sin necesidad de escribir el casting.
- **De un tipo más general a uno más específico**: aquí sí es obligatorio escribir el casting de forma explícita, porque Java no puede garantizar por sí solo que esa conversión sea válida.

```java
Object texto = "Hola";
String cadena = (String) texto;
```

En este ejemplo, `texto` está declarado como `Object`, un tipo más general. Al hacer `(String) texto`, se le indica a Java que trate ese valor concretamente como un `String`.

Si el casting entre objetos no es válido —por ejemplo, si el objeto real no es realmente del tipo al que se intenta convertir—, el programa lanzará un error en tiempo de ejecución.