### `reduce`

`reduce` es una **operación terminal de un `Stream`** que permite **combinar todos sus elementos para producir un único resultado**.

Mientras que `map` transforma cada elemento individual y `collect` reúne los elementos en una estructura, `reduce` tiene como objetivo **reducir varios elementos a un solo valor**.

Conceptualmente:

```
Elementos
   ↓
1 → 2 → 3 → 4 → 5
 \   \   \   \   \
  └─── combinar ───┘
            ↓
           15
```

Para realizar esta combinación, `reduce` utiliza una operación que indica **cómo combinar dos valores para obtener el siguiente resultado parcial**.

```java
int suma = numeros.stream()
        .reduce(0, (a, b) -> a + b);
```

En este caso, el `0` es el **valor inicial** y la lambda define cómo se van acumulando los elementos.

Conceptualmente:

```
0 + 1 → 1
1 + 2 → 3
3 + 3 → 6
6 + 4 → 10
10 + 5 → 15
```

El resultado final es un único valor.

La operación utilizada para combinar los elementos es importante porque debe permitir que la reducción produzca un resultado coherente. Esto es especialmente relevante cuando Java puede realizar el procesamiento de forma paralela.

`reduce` puede utilizarse para obtener diferentes tipos de resultados, no solamente números. Lo importante es que exista una operación que permita **combinar progresivamente los elementos**.

Por ejemplo, conceptualmente podemos pasar de:

```
Stream
→ A
→ B
→ C
→ D
```

a:

```
A + B + C + D
       ↓
   resultado
```

La diferencia fundamental con `collect` es:

```
collect
→ reúne elementos en una estructura o resultado acumulado

reduce
→ combina elementos para producir un único resultado
```

>`reduce` permite **combinar los elementos de un `Stream` progresivamente hasta obtener un único resultado**, utilizando una operación de reducción que define cómo se combinan los valores.