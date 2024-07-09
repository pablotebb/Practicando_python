```python
mi_lista = [1, 2, 10, 4]

for i in mi_lista:
    print(f"i vale {i}")
```

    i vale 1
    i vale 2
    i vale 10
    i vale 4
    


```python
mi_lista = [1, "hola", 2, "adios"]

for i in mi_lista:
    print(f"i vale {i}")
```

    i vale 1
    i vale hola
    i vale 2
    i vale adios
    


```python
mi_tupla = (1, "hola", 2, "adios")

for i in mi_tupla:
    print(f"i vale {i}")
```

    i vale 1
    i vale hola
    i vale 2
    i vale adios
    


```python
mi_dicc = {"nombre": "Pablo", "apellido": "Lopez", "telefono": 4343434}

for clave in mi_dicc:
    print(f"clave vale: {clave}, y mi_dicc[clave] vale: {mi_dicc[clave]}")
```

    clave vale: nombre, y mi_dicc[clave] vale: Pablo
    clave vale: apellido, y mi_dicc[clave] vale: Lopez
    clave vale: telefono, y mi_dicc[clave] vale: 4343434
    


```python
mi_cadena = "1230239409"

for i in mi_cadena:
    print(f"i vale {i}")
```

    i vale 1
    i vale 2
    i vale 3
    i vale 0
    i vale 2
    i vale 3
    i vale 9
    i vale 4
    i vale 0
    i vale 9
    


```python
mi_cadena = "Pablo Lopez Díaz"

for i in mi_cadena:
    print(f"i vale {i}")
```

    i vale P
    i vale a
    i vale b
    i vale l
    i vale o
    i vale  
    i vale L
    i vale o
    i vale p
    i vale e
    i vale z
    i vale  
    i vale D
    i vale í
    i vale a
    i vale z
    


```python
mi_cadena = "Pablo Lopez Díaz"

for i in range(len(mi_cadena)):
    print(f"i vale {i}, y mi_cadena[i] vale: {mi_cadena[i]}")
```

    i vale 0, y mi_cadena[i] vale: P
    i vale 1, y mi_cadena[i] vale: a
    i vale 2, y mi_cadena[i] vale: b
    i vale 3, y mi_cadena[i] vale: l
    i vale 4, y mi_cadena[i] vale: o
    i vale 5, y mi_cadena[i] vale:  
    i vale 6, y mi_cadena[i] vale: L
    i vale 7, y mi_cadena[i] vale: o
    i vale 8, y mi_cadena[i] vale: p
    i vale 9, y mi_cadena[i] vale: e
    i vale 10, y mi_cadena[i] vale: z
    i vale 11, y mi_cadena[i] vale:  
    i vale 12, y mi_cadena[i] vale: D
    i vale 13, y mi_cadena[i] vale: í
    i vale 14, y mi_cadena[i] vale: a
    i vale 15, y mi_cadena[i] vale: z
    


```python
series = [1, 0, 22, 45, 1, 2, 3]

for i in range(len(series)):
    print(f"i vale {i}, y series[i] vale {series[i]}")
```

    i vale 0, y series[i] vale 1
    i vale 1, y series[i] vale 0
    i vale 2, y series[i] vale 22
    i vale 3, y series[i] vale 45
    i vale 4, y series[i] vale 1
    i vale 5, y series[i] vale 2
    i vale 6, y series[i] vale 3
    


```python
palabras = ["uno", "dos", "tres", "cuatro"]

for i in range(len(palabras)):
    print(f"i vale {i} y palabras[i] vale {palabras[i]}")
```

    i vale 0 y palabras[i] vale uno
    i vale 1 y palabras[i] vale dos
    i vale 2 y palabras[i] vale tres
    i vale 3 y palabras[i] vale cuatro
    


```python
for i in range(8):
    print(f"i vale {i}")
```

    i vale 0
    i vale 1
    i vale 2
    i vale 3
    i vale 4
    i vale 5
    i vale 6
    i vale 7
    


```python
for i in range(1, 54):
    print(f"i vale {i}")
```

    i vale 1
    i vale 2
    i vale 3
    i vale 4
    i vale 5
    i vale 6
    i vale 7
    i vale 8
    i vale 9
    i vale 10
    i vale 11
    i vale 12
    i vale 13
    i vale 14
    i vale 15
    i vale 16
    i vale 17
    i vale 18
    i vale 19
    i vale 20
    i vale 21
    i vale 22
    i vale 23
    i vale 24
    i vale 25
    i vale 26
    i vale 27
    i vale 28
    i vale 29
    i vale 30
    i vale 31
    i vale 32
    i vale 33
    i vale 34
    i vale 35
    i vale 36
    i vale 37
    i vale 38
    i vale 39
    i vale 40
    i vale 41
    i vale 42
    i vale 43
    i vale 44
    i vale 45
    i vale 46
    i vale 47
    i vale 48
    i vale 49
    i vale 50
    i vale 51
    i vale 52
    i vale 53
    


```python
for i in range(1, 54, 3):
    print(f"i vale {i}")
```

    i vale 1
    i vale 4
    i vale 7
    i vale 10
    i vale 13
    i vale 16
    i vale 19
    i vale 22
    i vale 25
    i vale 28
    i vale 31
    i vale 34
    i vale 37
    i vale 40
    i vale 43
    i vale 46
    i vale 49
    i vale 52
    


```python
email = input("Introduce un email: ")
sw = 0

for i in range(len(email)):
    if email[i] == "@":
        print("El email es correcto")
        sw = 1
        break;

if sw == 0:
    print("Falta la @")

print("Adios!")
```

    Introduce un email:  juan@hotmail.com
    

    El email es correcto
    Adios!
    
