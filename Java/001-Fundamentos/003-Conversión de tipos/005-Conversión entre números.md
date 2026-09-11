# Conversión entre números

Java define varios tipos de datos numéricos (`byte`, `short`, `int`, `long`, `float`, `double`), y en muchas situaciones —al asignar un valor a una variable de otro tipo, al mezclar tipos en una misma operación, o al pasar un valor a un método que espera otro tipo numérico— es necesario convertir un valor de un tipo numérico a otro.

Estos tipos numéricos están ordenados según el espacio que ocupan en memoria y el rango de valores que pueden representar:

```text
byte → short → int → long → float → double
```

Cuando un valor se convierte hacia un tipo situado más a la derecha en este orden, la conversión es segura, porque el tipo destino puede representar todos los valores del tipo de origen. Cuando se convierte hacia un tipo situado más a la izquierda, existe riesgo de que el valor no quepa completamente o de perder parte de su información, por lo que Java trata esta conversión de forma distinta a la anterior.

Por esta diferencia de riesgo, Java distingue entre dos formas de realizar estas conversiones según la dirección en la que se produzcan, cada una con su propio comportamiento y reglas.