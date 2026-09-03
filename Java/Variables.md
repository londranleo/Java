Una variable no es más que un **espacio reservado en la memoria RAM** para almacenar un valor que puede cambiar durante la ejecución del programa.

En Java, para usar una variable, primero debemos **declararla** (decirle al sistema: “resérvame espacio para un entero”) e **inicializarla** (darle un valor).

```
//declaracion 
int edad;

//Inicializacion
edad = 25;

//Todo en una liena 
int puntuacion = 100;
```
### Tipos de Variables en Java

En Java, todo son Objetos... excepto los tipos primitivos.

Java mantiene 8tipos de tipos de datos básicos que **no** son objetos. Son valores puros que se almacenas directamente en la memoria _Stack_ (pila), lo que los hace extremadamente rápidos de procesar.  

Se divide en 4 grupos: Enteros, Flotantes, Caracteres y Booleanos.

**Números enteros (Integer types)**

sirve para contar cosas que no tienen decimales hay 4 tipos, dependiendo de lo grande que sea el numero que quieres guardar. 

| Tipo  | Tammano | Rango                            | Uso                                         |
| ----- | ------- | -------------------------------- | ------------------------------------------- |
| byte  | 8 bits  | -128 a 127                       | Datos binarios crudos / Array masivos       |
| short | 16 bits | -32,768 a 32,767                 | casi en desuso hoy en dia                   |
| int   | 32 bits | -2 mil millones a 2 mil millones | **El estandar**. Usalo por defecto          |
| long  | 64 bits | Gigantesco (9 trillones...)      | Para IDs de base de datos, timestamps, etc. |
El tipo habitual es `int`. En Java, cuando escribes un numero `10` en el código, el copilador asume que es un `int`.

> [!NOTE] Nota
> Si quieres usar `long`, debes poner una "L" al final del numero, porque si no, Java intentara tratarlo como un `int` y si es muy grande, dara error.

```
int habitaciones = 12345678;
long distanciaEstrella = 9460730472580800L
```

**Números decimales** (Floating point types)

Para cada numero con partes fraccionaria se utiliza el estándar **IEEE 754** .

| TIPO   | TAMANO  | PRECISION       | USO                                               |
| ------ | ------- | --------------- | ------------------------------------------------- |
| float  | 32 bits | 6-7 decimales   | Gráficos 3D, arrays de datos cientificos          |
| double | 64 bits | 15-16 decimales | **El estándar**. Úsalo para matematicas generales |
Al igual que con los enteros, hay un estandar que es `double`. Java trata cualquier decimal (`3.14`) como un` double` por defecto. Si quieres forzar un `float`, debes usar la 'f'.

```
double pi = 3.1415926535;
float gravedad = 9.8f; 
```



# Sintaxis
para definir una variable , se debe especifar el tipo de dato, seguido del nombre y el valor se puede asignar al momento de la declacion o posteriormente 

```
Tipo nombreVarible = valor;
```

[[001-Ejemplos]]


