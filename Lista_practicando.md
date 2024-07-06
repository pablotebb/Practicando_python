## Listas

Ejemplos:


```python
lista = [1, 2, "hola", "adios", True]
print(lista)
print(lista[:])
```

    [1, 2, 'hola', 'adios', True]
    [1, 2, 'hola', 'adios', True]
    


```python
print(lista[:-1])
print(lista[2:-1])
print(lista[2:])
```

    [1, 2, 'hola', 'adios']
    ['hola', 'adios']
    ['hola', 'adios', True]
    


```python
lista.append("juan")
print(lista)
```

    [1, 2, 'hola', 'adios', True, 'juan']
    


```python
lista.append("jordi")
print(lista[:])
```

    [1, 2, 'hola', 'adios', True, 'juan', 'jordi']
    


```python
lista.extend(["uno", "dos", 3])
print(lista)
```

    [1, 2, 'hola', 'adios', True, 'juan', 'jordi', 'uno', 'dos', 3]
    


```python
# hice varios insert, por eso sale otro resultado
lista.insert(2, "domingo")
print(lista)
```

    [1, 2, 'domingo', 'domingo', 'pepe', 'pepe', 'pepe', 'pepe', 'hola', 'adios', True, 'juan', 'jordi', 'uno', 'dos', 3]
    


```python
lista.insert(0, "dionisio")
print(lista)
```

    ['dionisio', 1, 2, 'domingo', 'domingo', 'pepe', 'pepe', 'pepe', 'pepe', 'hola', 'adios', True, 'juan', 'jordi', 'uno', 'dos', 3]
    


```python
print(lista.index("pepe"))
print(lista.index("hola"))
```

    5
    9
    


```python
lista.remove("pepe")
print(lista)
```

    ['dionisio', 1, 2, 'domingo', 'domingo', 'pepe', 'pepe', 'hola', 'adios', True, 'juan', 'jordi', 'uno', 'dos', 3]
    


```python
# hice el pop varias veces, por eso quito los 3 últimos
lista.pop()
print(lista)
lista.reverse()
print(lista)
print(lista.count("pepe"))
print(lista.count("domingo"))
print(lista.count(2))
```

    [True, 'adios', 'hola', 'pepe', 'pepe', 'domingo', 'domingo', 2]
    [2, 'domingo', 'domingo', 'pepe', 'pepe', 'hola', 'adios', True]
    2
    2
    1
    


```python
lista2 = [55, 3, 1, 9, 88, 33, 1]
print(lista2)
print(lista2[:])
```

    [55, 3, 1, 9, 88, 33, 1]
    [55, 3, 1, 9, 88, 33, 1]
    


```python
lista2.sort()
print(lista2)
```

    [1, 1, 3, 9, 33, 55, 88]
    


```python
lista3 = ["Juan", "Pepe", "Alberto", "Cristina", "Ana", "Ramon"]
print(lista3)
lista3.sort()
print(lista3)
```

    ['Juan', 'Pepe', 'Alberto', 'Cristina', 'Ana', 'Ramon']
    ['Alberto', 'Ana', 'Cristina', 'Juan', 'Pepe', 'Ramon']
    


```python
print(type(lista))
print(type(lista2))
print(type(lista3))
```

    <class 'list'>
    <class 'list'>
    <class 'list'>
    


```python
print(lista3.__class__)
```

    <class 'list'>
    


```python
lista4 = lista3.copy()
lista3.append("fin")
print(lista3)
print(lista4)
```

    ['Alberto', 'Ana', 'Cristina', 'Juan', 'Pepe', 'Ramon', 'fin', 'fin']
    ['Alberto', 'Ana', 'Cristina', 'Juan', 'Pepe', 'Ramon', 'fin']
    


```python
print(dir(lista))
```

    ['__add__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getstate__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
    
