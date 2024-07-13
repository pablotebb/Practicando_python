# Clases


```python
class Coche():
    def __init__(self):
        self.__largo = 300
        self.__ancho = 200
        self.__ruedas = 4
        self.__arrancado = False
        self.__comprueba_test = False

    def arrancar(self, arranque):
        self.__arrancado = arranque

        if self.__arrancado:
            self.__comprueba_test = self.__chequeo()

        if self.__arrancado and self.__comprueba_test:
            print("Arrancando coche...")
        elif self.__arrancado and self.__comprueba_test == False:
            print("Test incorrecto de arranque")
        else:
            print("Apagamos coche...")

    def info(self):
        print(f"El coche tiene un largo de {self.__largo}, un ancho de {self.__ancho} y {self.__ruedas} ruedas")

    def __chequeo(self):
        self.gasolina = "Ok"
        self.aceite = "Ok"
        self.presion = "Ok"

        if self.gasolina == "Ok" and self.aceite == "Ok" and self.presion == "Ok":
            print("Chequeo correcto...")
            return True
        else:
            return False



coche = Coche()
coche.arrancar(True)
coche.info()
coche.arrancar(False)
print("------------------------")


coche2 = Coche()
coche.arrancar(False)
# coche.chequeo()    # No funciona!
# coche.ruedas = 2   # No funciona!
coche.info()

```

    Chequeo correcto...
    Arrancando coche...
    El coche tiene un largo de 300, un ancho de 200 y 4 ruedas
    Apagamos coche...
    ------------------------
    Apagamos coche...
    El coche tiene un largo de 300, un ancho de 200 y 4 ruedas
    


### Herencia


```python
class Vehiculo():
    def __init__(self, marca, modelo):
        self.marca = marca
        self.modelo = modelo
        self.arranque = False
        self.aceleracion = False
        self.frenada = False

    def arrancar(self):
        self.arranque = True

    def acelerar(self):
        self.aceleracion = True

    def frenar(self):
        self.frenada = True

    def info(self):
        print(f"""
        Vehículo
        --------

        Marca:  {self.marca}
        Modelo: {self.modelo}
        
        arranque:    {self.arranque}
        aceleracion: {self.aceleracion}
        frenada:     {self.frenada}
        
        """)

class Moto(Vehiculo):
    pass

moto = Moto("Honda", "1270")
moto.info()
moto.arrancar()
moto.acelerar()
moto.frenar()
moto.info()

moto2 = Moto("Kawasaky", "1000")
moto2.info()
moto2.arrancar()
moto2.acelerar()
moto2.frenar()
moto2.info()
```

    
            Vehículo
            --------
    
            Marca:  Honda
            Modelo: 1270
            
            arranque:    False
            aceleracion: False
            frenada:     False
            
            
    
            Vehículo
            --------
    
            Marca:  Honda
            Modelo: 1270
            
            arranque:    True
            aceleracion: True
            frenada:     True
            
            
    
            Vehículo
            --------
    
            Marca:  Kawasaky
            Modelo: 1000
            
            arranque:    False
            aceleracion: False
            frenada:     False
            
            
    
            Vehículo
            --------
    
            Marca:  Kawasaky
            Modelo: 1000
            
            arranque:    True
            aceleracion: True
            frenada:     True
            
            
    


```python
class Vehiculo():
    def __init__(self, marca, modelo):
        self.marca = marca
        self.modelo = modelo
        self.arranque = False
        self.aceleracion = False
        self.frenada = False

    def arrancar(self):
        self.arranque = True

    def acelerar(self):
        self.aceleracion = True

    def frenar(self):
        self.frenada = True

    def info(self):
        print(f"""
        Vehículo
        --------

        Marca:  {self.marca}
        Modelo: {self.modelo}
        
        arranque:    {self.arranque}
        aceleracion: {self.aceleracion}
        frenada:     {self.frenada}
        
        """)

class Moto(Vehiculo):
    def hcaballito(self, caballo):
        self.__caballito = caballo
        if self.__caballito:
            return "La moto hace el caballito"
        return
    def info(self):
         print(f"""
            Vehículo
            --------
    
            Marca:  {self.marca}
            Modelo: {self.modelo}
            
            arranque:    {self.arranque}
            aceleracion: {self.aceleracion}
            frenada:     {self.frenada}

            caballito:   {self.hcaballito(True)}
            
            """)

class Vehiculo_electrico(Vehiculo):
    def __init__(self, marca, modelo):
        super().__init__(marca, modelo) 
        self.bateria = False

    def cargar_bateria(self):
        self.bateria = True
        return "Bateria cargada"


class Bicicleta_electrica(Vehiculo_electrico, Vehiculo):
     def info(self):
         print(f"""
            Vehículo
            --------
    
            Marca:  {self.marca}
            Modelo: {self.modelo}
            
            arranque:    {self.arranque}
            aceleracion: {self.aceleracion}
            frenada:     {self.frenada}

            bateria:     {self.cargar_bateria()}
            
            """)
        
    

moto = Moto("Honda", "1270")
moto.arrancar()
moto.acelerar()
moto.frenar()
moto.info()


moto2 = Moto("Kawasaky", "1000")
moto2.arrancar()
moto2.acelerar()
moto2.frenar()
moto2.info()

bicicleta = Bicicleta_electrica("chopper", "123")
bicicleta.arrancar()
bicicleta.acelerar()
bicicleta.frenar()
bicicleta.info()
```

    
                Vehículo
                --------
        
                Marca:  Honda
                Modelo: 1270
                
                arranque:    True
                aceleracion: True
                frenada:     True
    
                caballito:   La moto hace el caballito
                
                
    
                Vehículo
                --------
        
                Marca:  Kawasaky
                Modelo: 1000
                
                arranque:    True
                aceleracion: True
                frenada:     True
    
                caballito:   La moto hace el caballito
                
                
    
                Vehículo
                --------
        
                Marca:  chopper
                Modelo: 123
                
                arranque:    True
                aceleracion: True
                frenada:     True
    
                bateria:     Bateria cargada
                
                
    

### Uso de super()
Principio de sustitución - Una empleado **es siempre** una persona, pero una persona **no es siempre** un empleado


```python
class Persona():
    def __init__(self, nombre, telefono, direccion):
        self.nombre = nombre
        self.telefono = telefono
        self.direccion = direccion

    def info(self):
        print(f"""
            nombre:    {self.nombre}
            telefono : {self.telefono}
            dirección: {self.direccion}
        """)

class Empleado(Persona):
    def __init__(self, profesion, salario, nombre, telefono, direccion):
        super().__init__(nombre, telefono, direccion)
        self.profesion = profesion
        self.salario = salario

    def info(self):
        super().info()
        print(f"""
            profesion: {self.profesion}
            salario:   {self.salario}
        """)

juan = Empleado("administrativo", "2000", "Juan", "3423433", "Calle de la X")
juan.info()
print("El objeto juan es instancia de Empleado: ", isinstance(juan, Empleado))
print("El objeto juan es instancia de Persona: ", isinstance(juan, Persona))
print("-------------------------------------")
pepe = Persona("Pepe", "3423443", "Calle de la J")
pepe.info()
print("El objeto pepe es instancia de Persona: ", isinstance(pepe, Persona))
print("El objeto pepe es instancia de Empleado: ", isinstance(pepe, Empleado))

```

    
                nombre:    Juan
                telefono : 3423433
                dirección: Calle de la X
            
    
                profesion: administrativo
                salario:   2000
            
    El objeto juan es instancia de Empleado:  True
    El objeto juan es instancia de Persona:  True
    -------------------------------------
    
                nombre:    Pepe
                telefono : 3423443
                dirección: Calle de la J
            
    El objeto pepe es instancia de Persona:  True
    El objeto pepe es instancia de Empleado:  False
    


### Polimorfismo

(Sin usar polimorfismo)


```python
class Coche():
    def desplazamiento(self):
        print("Soy un coche y me desplazo con 4 ruedas")

class Moto():
    def desplazamiento(self):
        print("Soy una moto y me desplazo con 2 ruedas")

class Camion():
    def desplazamiento(self):
        print("Soy un camión y me desplazo con 6 ruedas")

coche = Coche()
coche.desplazamiento()
moto = Moto()
moto.desplazamiento()
camion = Camion()
camion.desplazamiento()
```

    Soy un coche y me desplazo con 4 ruedas
    Soy una moto y me desplazo con 2 ruedas
    Soy un camión y me desplazo con 6 ruedas
    

(Usando polimorfismo)


```python
def vehiculo(vehiculo):
    vehiculo.desplazamiento()

objeto = Coche()  # puedes susutituir Coche() por Camion() o por Moto()
vehiculo(objeto)  # Polimorfismo
```

    Soy un coche y me desplazo con 4 ruedas
    


```python

```
