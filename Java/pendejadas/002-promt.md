Quiero que me ayudes a crear mi **documentación de teoría de Java**.

Ya tengo creada mi propia **ruta de aprendizaje**, organizada por temas y subtemas. Yo iré trabajando los temas uno por uno.

## Cómo te proporcionaré los temas

Yo te proporcionaré únicamente el nombre del tema.

Por ejemplo:

```text
Características principales
```

o:

```text
Qué es una variable
```

No necesito darte ninguna explicación adicional ni contexto.

Debes interpretar directamente el texto que te proporcione como **el tema exacto que tienes que documentar** y comenzar directamente con su explicación.

---

## Objetivo de la documentación

Estoy creando una documentación que utilizaré principalmente como **guía de consulta y repaso**.

Es posible que después de varios meses sin utilizar un concepto olvide parte de lo aprendido. Quiero poder entrar en mi documentación, leer el tema y recuperar rápidamente los conocimientos necesarios.

Por eso quiero que la documentación sea:

- Completa.
    
- Correcta técnicamente.
    
- Fácil de entender.
    
- Fácil de leer.
    
- Fácil de recordar.
    
- Compacta.
    
- Útil para consultar posteriormente.
    

No quiero un libro académico ni explicaciones excesivamente largas.

**Compacto no significa incompleto.**

Debes incluir toda la información importante necesaria para comprender correctamente el tema, pero expresándola de la forma más sencilla y directa posible.

---

## Redacción

Escribe pensando en una persona que **no tiene conocimientos previos de programación**.

La explicación debe utilizar un lenguaje:

- Natural.
    
- Amigable.
    
- Claro.
    
- Sencillo.
    
- Profesional.
    
- Fácil de seguir.
    

Evita una redacción excesivamente académica o técnica.

Si puedes explicar correctamente un concepto utilizando palabras sencillas, hazlo.

Cuando sea necesario utilizar un término técnico, explícalo de forma sencilla dentro de la propia explicación.

Quiero que una persona que está empezando pueda leer la documentación y entenderla sin tener que buscar constantemente el significado de otros conceptos.

---

## Profundidad

Quiero suficiente profundidad para **entender realmente el concepto**, no simplemente memorizar una definición.

Explica lo importante del tema, especialmente:

- Qué es.
    
- Cómo funciona.
    
- Cómo se comporta.
    
- Qué papel cumple.
    
- Qué aspectos son importantes para utilizarlo o entenderlo.
    

Pero no añadas información únicamente para hacer la explicación más larga.

No repitas una misma idea varias veces con diferentes palabras.

Busca siempre este equilibrio:

```text
Información completa
        +
Explicación sencilla
        +
Poca repetición
        +
Longitud razonable
```

---

# Límite estricto del tema

Esta es una de las reglas más importantes.

**El título que te proporcione define exactamente el límite de la explicación.**

Debes explicar únicamente el concepto indicado por ese título.

Mi ruta ya está organizada y cada concepto tendrá su propio apartado.

Por ejemplo, si mi ruta contiene:

```text
Variables
├── Qué es una variable
├── Declaración de variables
├── Inicialización
├── Tipos de variables
└── ...
```

y yo te digo:

```text
Qué es una variable
```

debes explicar **únicamente qué es una variable**.

No debes explicar ni desarrollar:

```text
Declaración de variables
Inicialización
Tipos de variables
Ámbito de las variables
```

aunque estén relacionados con las variables.

No debes adelantar contenido de los siguientes apartados.

Tampoco debes introducir otro concepto simplemente porque pueda servir como una explicación adicional.

### Regla

**Explica el tema, no sus temas vecinos.**

Si otro concepto tiene o puede tener su propio apartado dentro de mi ruta, **no lo desarrolles dentro del tema actual**.

Si es absolutamente necesario mencionar otro concepto para que la explicación sea comprensible, puedes nombrarlo brevemente, pero no debes explicar su funcionamiento ni desarrollar su teoría.

Por ejemplo, si estoy documentando:

```text
Qué es una variable
```

no quiero que después de explicar qué es una variable añadas:

```text
Para utilizar una variable primero debemos declararla...
```

Eso pertenece al tema:

```text
Declaración de variables
```

Por tanto, debe omitirse.

Cada tema debe poder funcionar como una **pieza independiente de mi documentación**, sin invadir el contenido de los demás temas.

---

## No convertir el tema en una introducción general

No quiero que amplíes automáticamente el contenido para convertirlo en una explicación general de Java.

Si te doy:

```text
Qué es Java
```

habla de qué es Java.

Si te doy:

```text
Características principales
```

habla de las características principales.

Si te doy:

```text
JVM
```

habla de la JVM.

No mezcles los temas entre sí.

---

## Estructura

Quiero una estructura **compacta y natural**.

No conviertas cada pequeña idea en una pregunta o apartado.

Evita estructuras como:

```text
¿Qué es?
¿Para qué sirve?
¿Cómo funciona?
¿Por qué existe?
¿Cuándo se utiliza?
```

si esas ideas pueden explicarse de forma natural dentro de una misma explicación.

Utiliza títulos o subtítulos únicamente cuando realmente ayuden a organizar el contenido.

Prefiero una explicación conectada y fácil de leer antes que muchos apartados pequeños.

---

## Ejemplos

Utiliza **pocos ejemplos**.

Un ejemplo debe utilizarse únicamente cuando realmente ayude a entender o recordar el concepto.

No añadas ejemplos solo para hacer más grande la explicación.

Cuando utilices código, debe ser código real y sencillo:

```java
int edad = 25;
```

El código debe estar relacionado directamente con el tema actual.

**No utilices un ejemplo que obligue a explicar otro tema de mi ruta.**

Si para mostrar un ejemplo tienes que introducir un concepto que todavía no corresponde al tema actual, utiliza otro ejemplo o explica el concepto sin ejemplo.

---

## Código

Cuando muestres código Java:

- Utiliza código correcto.
    
- Mantén los ejemplos pequeños.
    
- No añadas código innecesario.
    
- Explica únicamente las partes relevantes para el tema actual.
    
- No aproveches el ejemplo para explicar otros conceptos.
    

El código está para ayudar a comprender la teoría, no para sustituirla.

---

## No repetir la información

No repitas al final lo que ya has explicado.

No quiero secciones como:

```text
Resumen
En resumen
Conclusión
Para recordar
Recuerda
Conceptos clave
```

La explicación debe terminar cuando termine de explicarse el tema.

No repitas la definición del principio al final.

---

## Formato de salida

Esta regla es MUY IMPORTANTE.

La respuesta completa debe estar dentro de **un único bloque de texto copiable**.

Quiero poder utilizar el botón de copiar del bloque y copiar **toda la documentación de una sola vez**.

Todo el contenido debe estar preparado para poder copiarlo directamente a mis archivos de documentación.

Utiliza Markdown dentro del bloque.

Por ejemplo:

```markdown
# Qué es una variable

Una variable es...
```

### Fuera del bloque no debe haber absolutamente nada.

No escribas:

- "Aquí tienes..."
    
- "Perfecto."
    
- Introducciones.
    
- Explicaciones sobre lo que vas a hacer.
    
- Comentarios.
    
- Preguntas.
    
- Recomendaciones.
    
- Despedidas.
    
- "Espero que te sirva."
    
- "Si quieres podemos..."
    
- Cualquier otro texto adicional.
    

**La única salida permitida es la documentación del tema.**

---

## Markdown

Dentro del bloque puedes utilizar:

- `#` para el título.
    
- `##` cuando realmente sea necesario dividir una parte importante.
    
- **Negritas** para conceptos importantes.
    
- Listas cuando faciliten realmente la lectura.
    
- Bloques de código para ejemplos.
    
- Diagramas de texto cuando ayuden a explicar un funcionamiento.
    

No abuses de estos elementos.

La documentación debe mantenerse limpia, compacta y fácil de consultar.

---

## No hagas preguntas

No me preguntes qué quiero que expliques.

No me preguntes cuánto detalle quiero.

No me preguntes si quiero ejemplos.

No me pidas contexto adicional.

Yo te proporcionaré únicamente el nombre del tema y debes encargarte de desarrollar la documentación siguiendo todas estas reglas.

---

## Regla principal

Cuando te proporcione un tema, piensa:

> **"Tengo que documentar exactamente este concepto y nada más."**

Debes incluir toda la información necesaria para comprenderlo correctamente, pero debes detenerte antes de entrar en conceptos que pertenecen a otros apartados.

La documentación debe ser:

**completa + sencilla + compacta + clara + técnicamente correcta + estrictamente centrada en el tema.**

Yo te proporcionaré los temas uno por uno.

No cambies mi ruta, no inventes nuevos apartados y no adelantes contenido de otros temas.