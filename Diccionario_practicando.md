## Diccionarios


```python
mi_diccionario = {"nombre": "Pepe", "apellido": "Lopez", "tfno": "93232333", "edad": 54}
print(mi_diccionario)
print()
print(dir(mi_diccionario))
```

    {'nombre': 'Pepe', 'apellido': 'Lopez', 'tfno': '93232333', 'edad': 54}
    
    ['__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getstate__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__ior__', '__iter__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__or__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__ror__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'clear', 'copy', 'fromkeys', 'get', 'items', 'keys', 'pop', 'popitem', 'setdefault', 'update', 'values']
    


```python
# Vemos claves
print(mi_diccionario.keys())
print()
# Vemos valores
print(mi_diccionario.values())
print()
print(len(mi_diccionario))
```

    dict_keys(['nombre', 'apellido', 'tfno', 'edad', 'direccion'])
    
    dict_values(['Pepe', 'Pérez', '93232333', 54, 'Sevilla'])
    
    5
    


```python
# Añadimos
mi_diccionario["direccion"] = "Madrid"
print(mi_diccionario)
# Modificamos
mi_diccionario["apellido"] = "Pérez"
mi_diccionario["direccion"] = "Sevilla"
print(mi_diccionario)
```

    {'nombre': 'Pepe', 'apellido': 'Lopez', 'tfno': '93232333', 'edad': 54, 'direccion': 'Madrid'}
    {'nombre': 'Pepe', 'apellido': 'Pérez', 'tfno': '93232333', 'edad': 54, 'direccion': 'Sevilla'}
    


```python
# Listar un elemento
print(mi_diccionario["apellido"])
```

    Pérez
    


```python
# Borramos un elemento 
del mi_diccionario["apellido"]
print(mi_diccionario)
```

    {'nombre': 'Pepe', 'tfno': '93232333', 'edad': 54, 'direccion': 'Sevilla'}
    


```python
mi_tupla = ("nombre", "apellido", "direccion")
mi_diccionario2 = {mi_tupla[0]: "Pepino", mi_tupla[1]: "Díaz", mi_tupla[2]: "Madrid", 3: "Parado", "dias_cotizados": (134, 123, 565, 123, 58)}
print(mi_diccionario2)
```

    {'nombre': 'Pepino', 'apellido': 'Díaz', 'direccion': 'Madrid', 3: 'Parado', 'dias_cotizados': (134, 123, 565, 123, 58)}
    


```python
print(mi_diccionario2[mi_tupla[0]])
print(mi_diccionario2["nombre"])
print(mi_diccionario2["dias_cotizados"])
print(mi_diccionario2["dias_cotizados"][0])
print(mi_diccionario2["dias_cotizados"][1])
```

    Pepino
    Pepino
    (134, 123, 565, 123, 58)
    134
    123
    


```python
print(mi_diccionario2.__class__)
print(type(mi_diccionario2))
```

    <class 'dict'>
    <class 'dict'>
    


```python

```
