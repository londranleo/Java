# LocalDate

`LocalDate` es una clase de Java que representa **una fecha sin información de hora ni zona horaria**.

Forma parte del paquete `java.time`, que proporciona las clases modernas de Java para trabajar con fechas y horas.

Una `LocalDate` contiene tres componentes:

```
año → mes → día
```

Por ejemplo:

```
LocalDate fecha = LocalDate.of(2026, 9, 17);
```

En este caso, la fecha representa el **17 de septiembre de 2026**, pero no contiene ni hora ni información sobre la zona horaria.

`LocalDate` es apropiado cuando solo nos interesa una fecha del calendario, por ejemplo, una fecha de nacimiento, una fecha de vencimiento o una fecha de reserva.

Una característica importante es que `LocalDate` es **inmutable**. Esto significa que una vez creada una fecha, sus valores no se modifican directamente. Las operaciones que aparentemente modifican la fecha producen una **nueva instancia**.

```
LocalDate fecha = LocalDate.of(2026, 9, 17);
LocalDate siguiente = fecha.plusDays(1);
```

Conceptualmente:

```
fecha
2026-09-17

      ↓ plusDays(1)

nueva fecha
2026-09-18
```

También permite realizar operaciones relacionadas con el calendario, como obtener partes de una fecha, añadir o restar tiempo y comparar fechas.

Es importante no confundir `LocalDate` con otras clases de `java.time`:

```
LocalDate
→ fecha

LocalTime
→ hora

LocalDateTime
→ fecha + hora

ZonedDateTime
→ fecha + hora + zona horaria
```