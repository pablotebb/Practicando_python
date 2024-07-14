# Cadenas:
[enlace a cadenas](https://pyspanishdoc.sourceforge.net/lib/string-methods.html)


```python
nombre = "pablo lópez díaz"

print(dir(nombre))
```

    ['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__getstate__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'removeprefix', 'removesuffix', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
    


```python
print(nombre.capitalize())
```

    Pablo lópez díaz
    


```python
print(nombre.upper())
```

    PABLO LÓPEZ DÍAZ
    


```python
print(nombre.lower())
```

    pablo lópez díaz
    


```python
print(nombre.center(130))
```

                                                             pablo lópez díaz                                                         
    


```python
print(nombre.count("l"))
```

    2
    


```python
print(nombre.count("lópez"))
```

    1
    


```python
print(nombre.endswith("díaz"))
```

    True
    


```python
print(nombre.endswith("z"))
```

    True
    


```python
print(nombre.isnumeric())
numero = "dfdsf4dfdf"
print(numero.isnumeric())
numero2 = "3434e"
print(numero2.isnumeric())
numero3 = "34434"
print(numero3.isnumeric())
print(numero2.isdigit())
print(numero3.isdigit())
```

    False
    False
    False
    True
    False
    True
    


```python
print(nombre.islower())
otronombre = "Juan"
print(otronombre.islower())
```

    True
    False
    


```python
print(nombre.find("díaz"))
```

    12
    


```python
print(nombre.index("díaz"))
```

    12
    


```python
is_space = " "
print(is_space.isspace())
no_space = ""
print(no_space.isspace())
```

    True
    False
    


```python
print(nombre.split())
minombre = "    Pepe      "
print(minombre.strip())
```

    ['pablo', 'lópez', 'díaz']
    Pepe
    


```python
print(nombre)
print(nombre.replace("díaz", "jimenez"))
print(nombre.startswith("pablo"))
```

    pablo lópez díaz
    pablo lópez jimenez
    True
    


```python
print(nombre)
print(nombre.title())
```

    pablo lópez díaz
    Pablo López Díaz
    


```python
edad = input("Por favor, entra tu edad: ")

while(edad.isdigit() == False):
    print("Debes entrar un valor numérico!")
    edad = input("Por favor, entra tu edad: ")

if int(edad) < 18:
    print("Eres menor de edad")
else:
    print("Eres mayor de edad")
```

    Por favor, entra tu edad:  dfdfd
    

    Debes entrar un valor numérico!
    

    Por favor, entra tu edad:  dfdsfd
    

    Debes entrar un valor numérico!
    

    Por favor, entra tu edad:  17
    

    Eres menor de edad
    
