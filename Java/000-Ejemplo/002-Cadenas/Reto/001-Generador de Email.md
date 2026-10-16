## Enunciado

Crea un programa en Java que genere el correo electrónico corporativo de un empleado a partir de tres datos: **nombre completo**, **empresa** y **dominio**.

Los datos deben estar guardados en variables al principio del programa, de forma que se puedan **cambiar fácilmente** por otros sin tocar el resto del código.

## Datos de ejemplo

- **Nombre:** Ana Lopez Soto
- **Empresa:** Java Interprice
- **Dominio:** com.es

## Reglas para construir el correo

1. El nombre se escribe en **minúsculas** y los espacios entre palabras se sustituyen por **puntos**.
2. El nombre de la empresa se escribe en **minúsculas** y **sin espacios**.
3. El dominio se escribe en **minúsculas**.
4. El correo final tiene esta estructura: `nombre.apellidos@empresa.dominio`

## Limpieza de los datos

Los datos pueden venir con **espacios sobrantes al principio o al final** (por ejemplo, `"  Ana Lopez Soto  "`). El programa debe eliminarlos antes de construir el correo, de manera que **el resultado sea siempre el mismo**, tenga o no espacios de más.

## Resultado esperado

Con los datos de ejemplo, y también con esta versión con espacios:

```
Nombre:  "   Ana Lopez Soto  "
Empresa: " Java Interprice "
Dominio: "  com.es "
```

el programa debe mostrar exactamente:

```
Email: ana.lopez.soto@javainterprice.com.es
```
