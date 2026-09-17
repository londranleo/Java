### `LocalTime`

`LocalTime` es una clase de Java que representa **una hora sin información de fecha ni zona horaria**.

Forma parte del paquete `java.time` y está diseñada para trabajar únicamente con la parte horaria de un momento.

Una `LocalTime` puede representar:

```
hora → minuto → segundo → nanosegundo
```

Por ejemplo:

```
LocalTime hora = LocalTime.of(14, 30);
```

En este caso, la hora es `14:30`, pero no contiene información sobre qué día corresponde ni en qué zona horaria se encuentra.

`LocalTime` es apropiado cuando únicamente nos interesa una **hora del día**, como el horario de apertura de un establecimiento, una hora de una cita o el inicio de una actividad.

Al igual que `LocalDate`, `LocalTime` es **inmutable**. Las operaciones que modifican aparentemente una hora producen una nueva instancia en lugar de alterar la original.

```
LocalTime hora = LocalTime.of(14, 30);
LocalTime nuevaHora = hora.plusHours(2);
```

Conceptualmente:

```
14:30
  ↓ + 2 horas
16:30
```

También permite obtener sus diferentes componentes, realizar operaciones con horas y comparar diferentes valores de tiempo.

Es importante distinguirlo de las demás clases de `java.time`:

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