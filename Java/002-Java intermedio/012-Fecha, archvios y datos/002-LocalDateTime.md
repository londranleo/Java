### `LocalDateTime`

`LocalDateTime` es una clase de Java que representa **una fecha y una hora juntas, pero sin información de zona horaria**.

Forma parte del paquete `java.time` y combina las características de `LocalDate` y `LocalTime`.

Una `LocalDateTime` contiene:

```
fecha + hora
```

Por ejemplo:

```
LocalDateTime fechaHora = LocalDateTime.of(
    2026, 9, 17, 14, 30
);
```

El valor representa el **17 de septiembre de 2026 a las 14:30**, pero no indica en qué zona horaria se encuentra.

Esto es importante porque `LocalDateTime` describe una fecha y hora **locales**, no un instante absoluto en el tiempo.

Por ejemplo, `14:30` en Madrid y `14:30` en Tokio representan momentos diferentes, pero un `LocalDateTime` por sí solo no puede distinguirlos porque no contiene ninguna zona horaria.

`LocalDateTime` es apropiado cuando necesitamos trabajar conjuntamente con fecha y hora, pero **la zona horaria no forma parte de la información necesaria**.

Al igual que `LocalDate` y `LocalTime`, es **inmutable**. Las operaciones que aparentemente modifican el valor producen una nueva instancia.

```
LocalDateTime fechaHora = LocalDateTime.of(2026, 9, 17, 14, 30);
LocalDateTime nuevaFechaHora = fechaHora.plusHours(2);
```

Conceptualmente:

```
2026-09-17 14:30
        ↓ + 2 horas
2026-09-17 16:30
```

También permite obtener o modificar conceptualmente sus componentes de fecha y hora, así como comparar diferentes valores.

Es importante diferenciarlo de las otras clases:

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