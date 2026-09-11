# Widening

**Widening** es el término en inglés que se utiliza para referirse a una conversión que va de un tipo "más pequeño" o "más específico" hacia uno "más grande" o "más general". Es la palabra técnica que describe el tipo de conversión que Java realiza de forma automática, sin necesidad de casting.

Este concepto se aplica en dos contextos:

- **Con tipos numéricos**: cuando un valor pasa de un tipo que ocupa menos espacio a otro que ocupa más espacio (por ejemplo, de `int` a `double`), siguiendo el orden creciente entre los tipos numéricos.
- **Con objetos**: cuando una referencia de un tipo más específico se trata como una referencia de un tipo más general del que hereda.

En ambos casos, Java permite el widening de manera automática porque el tipo destino siempre puede representar o contener correctamente el valor de origen, sin riesgo de pérdida de información.

Widening es lo opuesto a **narrowing**, que es el término que describe la conversión en la dirección contraria (de un tipo más grande o específico a uno más pequeño o general), y que sí requiere una acción explícita por parte del programador.