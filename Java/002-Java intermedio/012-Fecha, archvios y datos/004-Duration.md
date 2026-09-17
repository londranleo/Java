### `Duration`

`Duration` es una clase de Java que representa una **cantidad de tiempo basada en segundos y nanosegundos**.

Forma parte del paquete `java.time` y está pensada para representar una duración de tiempo independiente del calendario.

A diferencia de `Period`, que utiliza años, meses y días, `Duration` utiliza unidades de tiempo como:

```
días → horas → minutos → segundos → nanosegundos
```

Por ejemplo:

```
Duration duracion = Duration.ofHours(3);
```

Esta duración representa **tres horas**, pero no está asociada a una fecha concreta.

También podemos crear una duración utilizando otras unidades:

```
Duration.ofMinutes(30);
Duration.ofSeconds(45);
```

Una característica importante es que `Duration` representa una cantidad de tiempo basada en **segundos y fracciones de segundo**, por lo que resulta adecuada para medir intervalos de tiempo.

Puede utilizarse, por ejemplo, para calcular cuánto tiempo ha pasado entre dos momentos:

```
Duration duracion = Duration.between(inicio, fin);
```

Conceptualmente:

```
inicio
  ↓
   transcurre tiempo
  ↓
fin
  ↓
Duration
  ↓
duración transcurrida
```

La diferencia fundamental con `Period` es la forma en que representan el tiempo:

```
Period
→ años, meses y días
→ basado en el calendario

Duration
→ segundos y fracciones de segundo
→ basado en una cantidad de tiempo
```

Esto es importante porque un mes no tiene siempre la misma duración, mientras que una cantidad expresada en segundos representa una duración concreta.

Al igual que las demás clases de `java.time`, `Duration` es **inmutable**. Las operaciones que modifican una duración producen una nueva instancia.