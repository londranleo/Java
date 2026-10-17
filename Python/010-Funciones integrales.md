Son funciones que Python ya trae incorporadas. Puedes utilizarlas directamente, sin tener que crearlas ni importar una biblioteca. 

|Función|¿Para qué sirve?|Ejemplo|
|---|---|---|
|`print()`|Mostrar datos|`print("Hola")`|
|`input()`|Pedir datos|`input("Nombre: ")`|
|`int()`|Convertir a entero|`int("5")` → `5`|
|`float()`|Convertir a decimal|`float("3.5")` → `3.5`|
|`str()`|Convertir a texto|`str(25)` → `"25"`|
|`len()`|Contar elementos|`len("Hola")` → `4`|
|`type()`|Saber el tipo de dato|`type(5)` → `int`|
|`max()`|Obtener el mayor|`max(3, 8, 2)` → `8`|
|`min()`|Obtener el menor|`min(3, 8, 2)` → `2`|
|`sum()`|Sumar elementos|`sum([1, 2, 3])` → `6`|
|`round()`|Redondear números|`round(3.7)` → `4`|
|`abs()`|Valor absoluto|`abs(-5)` → `5`|
```python
numeros = [4, 8, 2]

print(len(numeros))  # 3
print(max(numeros))  # 8
print(min(numeros))  # 2
print(sum(numeros))  # 14
```