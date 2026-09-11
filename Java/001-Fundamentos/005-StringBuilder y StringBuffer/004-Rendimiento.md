# Rendimiento

`StringBuilder` es más rápido que `StringBuffer`. La razón está en la sincronización: `StringBuffer` protege sus métodos para que puedan usarse de forma segura desde varios hilos a la vez, y esa protección obliga a comprobar y controlar el acceso cada vez que se modifica el objeto. `StringBuilder`, al no incluir esa protección, se ejecuta sin ese control adicional y por tanto de forma más rápida.

Esta diferencia de rendimiento solo se nota realmente cuando se realizan muchas operaciones sobre el texto (por ejemplo, dentro de bucles con miles de iteraciones). En programas donde solo se hacen unas pocas modificaciones, la diferencia es tan pequeña que no resulta relevante.

Comparado con `String`, tanto `StringBuilder` como `StringBuffer` son mucho más rápidos cuando se realizan varias modificaciones seguidas sobre el mismo texto, ya que evitan crear un objeto nuevo en cada cambio.