# Narrowing

**Narrowing** es el término en inglés que se utiliza para referirse a una conversión que va de un tipo "más grande" o "más general" hacia uno "más pequeño" o "más específico". Es la palabra técnica que describe el tipo de conversión que en Java requiere una acción explícita por parte del programador, ya que no se realiza de forma automática.

Este concepto se aplica en dos contextos:

- **Con tipos numéricos**: cuando un valor pasa de un tipo que ocupa más espacio a otro que ocupa menos espacio (por ejemplo, de `double` a `int`), siguiendo el orden decreciente entre los tipos numéricos.
- **Con objetos**: cuando una referencia de un tipo más general se trata como una referencia de un tipo más específico del que hereda.

En ambos casos, Java exige que el narrowing se indique de forma explícita porque el tipo destino no siempre puede representar correctamente el valor de origen, existiendo riesgo de pérdida de información o de un error si la conversión no es válida.

Narrowing es lo opuesto a **widening**, que es el término que describe la conversión en la dirección contraria (de un tipo más pequeño o general a uno más grande o específico), y que sí ocurre de manera automática.