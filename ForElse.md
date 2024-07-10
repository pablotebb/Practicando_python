```python
dni = "42000123M"

for i in dni:
    print(i, end="")
else:
    print(" has impreso tu dni")
```

    42000123M has impreso tu dni
    


```python
for i in dni:
    print(i, end="")
    if i == "M":
        break
else:
    print(" esta linea no sale")
```

    42000123M


```python
dni = "42000123M"

while True:
    print(dni, end="")
    dni = input("Dame tu dni: ")
    if dni == "":
        break
else: 
    print(" esta linea no sale")
    
    
```

    42000123M

    Dame tu dni:  324423443M
    

    324423443M

    Dame tu dni:  
    


```python
numero = 7

while numero > 0:
    print(numero)
    numero -= 1
else:
    print("final del bucle")
```

    7
    6
    5
    4
    3
    2
    1
    final del bucle
    


```python

```
