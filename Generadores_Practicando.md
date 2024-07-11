# GENERADORES
- A diferencia de las listas, ahorran memoria y tiempo (pues no recorren la lista completa)
- Son excelentes para el manejo de datos infinitos en una lista
- En vez de **return**, generalmente usan **yield**
- Este *yield*, lo que hace es generar un **Objeto Iterable**, que recibe los datos de la lista de 1 en 1, y luego los va devolviendo. Cada vez
  que devuelve un elemento, se queda en "Stanby", hasta que le vuelven a pedir el siguiente
- Los objetos que se devuelven pueden ser de diversa índole: Listas, valores numéricos, palabras, Tuplas, Diccionarios..  

# Uso tradicional de listas


```python
def dameLista(limite):
    lista = []
    i = 0

    while(i <= limite):
        lista.append(i * 2)
        i += 1

    return lista # devuelve toda la lista generada

print(dameLista(10))

```

    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
    

## Uso de Generador


```python
def generadorLista(limite):
    i = 0

    while(i <= limite):
        yield i*2
        i += 1

listaGenerada = generadorLista(10)

for i in listaGenerada:      # no hay ninguna diferencia en cuanto a las listas
    print(i, end=", ")
    
```

    0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 

# Beneficio del uso de Generador


```python
def generadorLista(limite):
    i = 0

    while(i <= limite):
        yield i*2
        i += 1

pares = generadorLista(10)

print(next(pares))    # ahorras espacio y tiempo, sólo devuelve 0, y se queda el yield en standby... (no recorre el resto de la lista)

print("más codigo...")

print(next(pares))    # idem...

print("más código...")

print(next(pares))    # idem...

```

    0
    más codigo...
    2
    más código...
    4
    

# Uso de YIELD FROM
- cuando usamos \*variable, nos estamos refiriéndonos a una Tupla, que admite valores indeterminados (osea, cualquier número de elementos)
- cuando usamos \*\*variable, nos estamos refiriéndonos a un Diccionario, que admite valores indeterminados (osea, cualquier número de elementos)
- **yield from** se usa para ahorarte el uso de 2 fors anidados

## Uso de función que recibe Tupla, sin Yield From


```python
def DameElementos(*elementos):
    for i in elementos:
        yield i

elemento = DameElementos("Madrid", "Barcelona", "Cadiz", "Sevilla")
print(next(elemento))
print(next(elemento))
```

    Madrid
    Barcelona
    

## Uso de función que recibe Tupla, sin Yield From, y con For anidados


```python
def DameElementos(*elementos):
    for elemento in elementos:
        for subelemento in elemento:
            yield subelemento

elemento = DameElementos("Madrid", "Barcelona", "Cadiz", "Sevilla")
print(next(elemento))
print(next(elemento))
```

    M
    a
    

## Uso de función que recibe Tupla, con Yield From (sin For anidados)


```python
def DameElementos(*elementos):
    for elemento in elementos:
        yield from elemento    # por tanto, es lo mismo que el anterior caso, y te ahorras código

elemento = DameElementos("Madrid", "Barcelona", "Cadiz", "Sevilla")
print(next(elemento))
print(next(elemento))
                 
```

    M
    a
    
