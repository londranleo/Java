# Problemas de conversión

Al convertir valores entre tipos, ya sea de forma implícita, explícita o mediante texto, pueden surgir varios problemas si no se hace con cuidado. Conocerlos ayuda a entender por qué a veces un programa no da el resultado esperado o falla directamente.

**Pérdida de precisión decimal.** Al convertir un tipo decimal a uno entero (por ejemplo, `double` a `int`), la parte decimal se descarta por completo, sin redondear. Un valor como `9.99` se convierte en `9`, no en `10`.

**Desbordamiento (overflow).** Al convertir un valor entre tipos numéricos enteros, si el valor de origen es demasiado grande para caber en el tipo destino, el resultado no lanza un error, sino que produce un número incorrecto e inesperado, ya que los bits que no caben se pierden.

**Errores de formato en texto.** Al convertir un `String` a un número, si el texto no tiene exactamente el formato numérico esperado (por ejemplo, contiene letras, espacios o símbolos no permitidos), la conversión falla y detiene el programa lanzando una excepción `NumberFormatException`.

**Errores de casting entre objetos.** Al hacer casting de un tipo de objeto más general a uno más específico, si el objeto no es realmente del tipo al que se intenta convertir, la conversión falla en tiempo de ejecución con un error de tipo `ClassCastException`.

En todos estos casos, el problema aparece porque la conversión asume algo sobre el valor de origen que en realidad no se cumple, ya sea su tamaño, su formato o su tipo real.

