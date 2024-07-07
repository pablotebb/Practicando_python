## Tuplas
Las listas son inmutables (no se pueden modificar, añadir, borrar...) <br>
Se usan porque ahorran memoria y son más rápidas, para casos en que no se tengan que modificar los datos


```python
mi_tupla = ("luis", 1, 34, 2)
print(type(mi_tupla))
print(dir(mi_tupla))
```

    <class 'tuple'>
    ['__add__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__getstate__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'count', 'index']
    


```python
print(mi_tupla)
```

    ('luis', 1, 34, 2)
    


```python
# Si modificamos la tupla, nos dará error
# mi_tupla[0] = "Pepe" # TypeError: 'tuple' object does not support item assignment
# Si añadimos también nos dará error
# mi_tupla.append("hola") # AttributeError: 'tuple' object has no attribute 'append'
```


```python
# Para modificar una Tupla, la tenemos que cambiar a Lista, modificarla, y luego cambiarla a Tupla
mi_lista = list(mi_tupla)
print(mi_lista)
mi_lista[0] = "Luison"
print(mi_lista)
mi_tupla = tuple(mi_lista)
print(mi_tupla)
```

    ['Luison', 1, 34, 2]
    ['Luison', 1, 34, 2]
    ('Luison', 1, 34, 2)
    


```python
print(len(mi_tupla))
print(mi_tupla.count("Luison"))
```

    4
    1
    


```python
print(mi_tupla.index(34))
print(mi_tupla.index(2))
                    
```

    2
    3
    


```python
# Se puede usar una tupla sin paréntesis, pero no es aconsejable...
mi_tupla2 = "Pepe", 3, 4, 2024   # empaquetado de tupla
print(mi_tupla2)
```

    ('Pepe', 3, 4, 2024)
    


```python
mi_tupla3 = ("Pepe", 3, 4, 2024)
nombre, dia, mes, agno = mi_tupla   # desempaquetado de tupla
print(f"""
nombre = {nombre}
dia    = {dia}
mes    = {mes}
agno   = {agno}
""")
```

    
    nombre = Luison
    dia    = 1
    mes    = 34
    agno   = 2
    
    


```python
# Tupla de un sólo elemento
mi_elemento = ("Domingo")   # no se registra como una tupla
print(mi_elemento)
mi_elemento2 = ("Domingo",) # con la coma, se registra como tupla
print(mi_elemento2)
```

    Domingo
    ('Domingo',)
    


```python

```
