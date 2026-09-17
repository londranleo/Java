### `HashMap`

`HashMap` es una **implementación de la interfaz `Map`**. Se utiliza para almacenar información mediante asociaciones de **clave → valor**.

Su característica principal es que utiliza una **tabla hash** para organizar las entradas. Esto permite realizar operaciones como buscar, añadir o eliminar elementos de forma muy eficiente en condiciones normales.

```java
Map<String, Integer> edades = new HashMap<>();

edades.put("Leo", 22);
edades.put("Ana", 25);
```

En un `HashMap`, las **claves son únicas**. Si se utiliza una clave que ya existe, el valor asociado a esa clave se sustituye.

El orden de los elementos **no está garantizado**. No debemos asumir que los elementos aparecerán en el mismo orden en el que fueron añadidos.

Otra característica importante es que `HashMap` permite utilizar **una clave `null`** y también permite valores `null`.

La eficiencia de `HashMap` depende de cómo se distribuyen las claves mediante sus valores hash. Por eso, para que funcione correctamente con objetos propios, es importante que `equals()` y `hashCode()` estén correctamente definidos.

La relación entre `Map` y `HashMap` es:

```
Map
 ↓
interfaz

HashMap
 ↓
implementación
```

Por eso normalmente se recomienda declarar la variable utilizando la interfaz:

```java
Map<String, Integer> edades = new HashMap<>();
```

>`HashMap` es una implementación de `Map` que almacena pares **clave → valor** utilizando hashing. Sus claves son únicas, no garantiza un orden concreto y está diseñado para realizar búsquedas, inserciones y eliminaciones de forma eficiente.