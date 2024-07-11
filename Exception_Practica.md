## Exception
- Se lanzan cuando tenemos un error de ejecución en el código
- Evita que el error, rompa el programa y no continue por la parte que funciona


```python
def suma(a, b):
    return a+b

def resta(a, b):
    return a-b

def multiplica(a, b):
    return a*b

def divide(a, b):
    try:
        return a/b
    except ZeroDivisionError:
        print("No puedes dividir por cero!")
        return "Operación es incorrecta!"

while(True):
    try:
        elemento1 = int(input("primer elemento: "))
        elemento2 = int(input("segundo elemento: "))
        break         # en cuanto los 2 elementos son correctos, sale del bucle
    except ValueError:
        print("Tienes que introducir cifras!...")


opcion = input("Entra acción (suma, resta, multiplicacion, division): ")

if opcion.lower() == "suma":
    print(suma(elemento1, elemento2))

elif opcion.lower() == "resta":
    print(resta(elemento1, elemento2))

elif opcion.lower() == "multiplicacion":
    print(multiplica(elemento1, elemento2))

elif opcion.lower() == "division":
    print(divide(elemento1, elemento2))

else:
    print("Opción incorrecta")

print("Por aquí, sigue el resto del código")
                
```

    primer elemento:  8
    segundo elemento:  0
    Entra acción (suma, resta, multiplicacion, division):  division
    

    No puedes dividir por cero!
    Operación es incorrecta!
    Por aquí, sigue el resto del código
    


```python
def dividir():
    try:
        op1 = float(input("1ª opción: "))
        op2 = float(input("2ª opción: "))
        print("El resultado es: " + str(op1/op2))
    except ZeroDivisionError:
        print("No se puede dividir por cero")
    except ValueError:
        print("Opción no válida")
    finally:
        print("Este reglón se ejecuta siempre")

dividir()
```

    1ª opción:  8
    2ª opción:  0
    

    No se puede dividir por cero
    Este reglón se ejecuta siempre
    


```python
def dividir():
    try:
        op1 = float(input("1ª opción: "))
        op2 = float(input("2ª opción: "))
        print("El resultado es: " + str(op1/op2))
    except:     # Es una excepción general, no es recomendable
        print("No es valido!")
    finally:
        print("Este reglón se ejecuta siempre")

dividir()
```

    1ª opción:  fdfdfdfdf
    

    No es valido!
    Este reglón se ejecuta siempre
    


```python
def descripcion_edad(edad):
    if edad < 0:
        raise TypeError("La edad no puede ser negativa!")
    elif edad < 20:
        print("Eres muy joven")
    elif edad < 40:
        print("Eres joven")
    elif edad < 65:
        print("Eres maduro")
    elif edad < 110:
        print("Cuidate!")

edad = int(input("Cual es tu edad?: "))
try:
    descripcion_edad(edad)
except TypeError as error:
    print(error)

print("más código por aquí...")
```

    Cual es tu edad?:  -5
    

    La edad no puede ser negativa!
    más código por aquí...
    


```python
import math

def raizcuadrada(num):
    if num < 0:
        raise TypeError("No puede ser menor que cero!")
    else:
        print("La raiz cuadrada es: " + str(math.sqrt(num)))

numero = int(input("Introduce un número: "))
try:
    raizcuadrada(numero)
except TypeError as err:
    print(err)

print("Final del programa")
```

    Introduce un número:  -56
    

    No puede ser menor que cero!
    Final del programa
    
