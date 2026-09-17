### `Period`

`Period` es una clase de Java que representa una **cantidad de tiempo expresada en años, meses y días**.

Forma parte del paquete `java.time` y está pensada principalmente para realizar cálculos relacionados con **fechas del calendario**.

A diferencia de `LocalDate`, que representa una fecha concreta, `Period` representa **una cantidad de tiempo entre fechas**.

Por ejemplo:

```
Period periodo = Period.of(2, 3, 10);
```

Este `Period` representa:

```
2 años
3 meses
10 días
```

Una característica importante es que `Period` utiliza **unidades basadas en el calendario**. Esto significa que un mes no se considera una cantidad fija de días, ya que los meses pueden tener diferentes duraciones.

Por eso `Period` es apropiado cuando queremos expresar conceptos como:

```
Period.ofMonths(6);
```

Es decir, **seis meses**, y no simplemente una cantidad determinada de días.

También puede utilizarse junto con `LocalDate` para realizar cálculos:

```
LocalDate fecha = LocalDate.of(2026, 9, 17);
LocalDate nuevaFecha = fecha.plus(Period.ofMonths(3));
```

Conceptualmente:

```
2026-09-17
     ↓ + 3 meses
2026-12-17
```

`Period` está orientado a **fechas**, por lo que sus unidades son años, meses y días. Para representar cantidades de tiempo basadas en horas, minutos, segundos o nanosegundos se utiliza `Duration`.

```
Period
→ años, meses y días

Duration
→ horas, minutos, segundos y nanosegundos
```