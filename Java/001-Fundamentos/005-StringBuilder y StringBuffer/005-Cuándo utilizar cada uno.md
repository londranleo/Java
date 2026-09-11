# Cuándo utilizar cada uno

La elección entre `String`, `StringBuilder` y `StringBuffer` depende de cómo se vaya a usar el texto:

- Usa **`String`** cuando el texto no va a cambiar, o solo se va a modificar una o dos veces. Para textos fijos o con pocas modificaciones, su simplicidad hace que sea la opción más cómoda.

- Usa **`StringBuilder`** cuando el texto se va a modificar varias veces (concatenaciones, inserciones, eliminaciones, etc.) y esas modificaciones ocurren dentro de una sola parte del programa, sin que varios hilos trabajen sobre el mismo objeto a la vez. Es la opción más habitual, ya que cubre la mayoría de los casos con el mejor rendimiento.

- Usa **`StringBuffer`** únicamente cuando el texto vaya a modificarse desde varios hilos al mismo tiempo, y sea necesario garantizar que esas modificaciones no generen errores o datos corruptos por accesos simultáneos.