## **¿Qué es el polimorfismo?**

La palabra "polimorfismo" significa "muchas formas" y en programación se refiere a  métodos/funciones/operadores con el mismo nombre que se pueden ejecutar en  muchos objetos o clases. El polimorfismo es un concepto de la programación  orientada a objetos que permite que un objeto pueda comportarse de diferentes maneras dependiendo del contexto en el que se encuentre. En Python, el  polimorfismo se refiere a la capacidad de un objeto para utilizar métodos de la clase  padre o de la propia clase de manera dinámica, es decir, en tiempo de ejecución. 

La sintaxis para implementar el polimorfismo en Python es sencilla. Basta con definir una clase base con métodos que puedan ser sobrescritos por sus subclases, y luego  crear varias subclases que redefinan esos métodos según sea necesario.

### Polimorfismo de función 
 
Un ejemplo de una función de Python que se puede utilizar en diferentes objetos es la len()función. 
 
#### Cadena 

Para cadenas `len()`devuelve el número de caracteres: 
##### Ejemplo  
```python
x = "Hello World!" 
 
print(len(x)) 
``` 
#### Tupla 

Para tuplas `len()`devuelve el número de elementos de la tupla: 

##### Ejemplo 
```python
mytuple = ("apple", "banana", "cherry") 
 
print(len(mytuple)) 
``` 
#### Diccionario 

Para diccionarios, `len()`devuelve el número de pares clave/valor en el diccionario: 
##### Ejemplo
```python 
thisdict = { 
  "brand": "Ford", 
  "model": "Mustang", 
  "year": 1964 
} 
 
print(len(thisdict))
```

### Polimorfismo de clase 
 
El polimorfismo se usa a menudo en métodos de clase, donde podemos tener varias  clases con el mismo nombre de método. 
Por ejemplo, digamos que tenemos tres clases: `Car`, `Boat` y `Plane`, y todas tienen un método llamado `move()`:

#### Ejemplo 
Diferentes clases con el mismo método: 
```python
class Car: 
  def __init__(self, brand, model): 
    self.brand = brand 
    self.model = model 
 
  def move(self): 
    print("Drive!") 
 
class Boat: 
  def __init__(self, brand, model): 
    self.brand = brand 
    self.model = model 
 
  def move(self): 
    print("Sail!") 
 
class Plane: 
  def __init__(self, brand, model): 
    self.brand = brand 
    self.model = model 
 
  def move(self): 
    print("Fly!") 
 
car1 = Car("Opel", "Zafira")       #Create a Car class 
boat1 = Boat("Miami", "Acros 2324") #Create a Boat class 
plane1 = Plane("An", "34")     #Create a Plane class 
 
for x in (car1, boat1, plane1): 
  x.move() 
```

###  Polimorfismo de clase de herencia
 
El polimorfismo de clase de herencia en Python se refiere a la capacidad de una clase hija de una clase padre para sobrescribir un método de la clase padre con su propia implementación. Esto permite que distintas clases que heredan de una misma clase base tengan comportamientos diferentes para un mismo método.

#### Sintaxis:

```python
class ClaseBase:
    def metodo(self):
        print("Método de la clase base")

class ClaseHija(ClaseBase):
    def metodo(self):
        print("Método de la clase hija")
```

En este ejemplo, la clase `ClaseHija` hereda de la clase `ClaseBase` y sobrescribe el método `metodo`, cambiando su implementación.

#### Ejemplo:

```python
base = ClaseBase()
base.metodo()  # Salida: "Método de la clase base"

hija = ClaseHija()
hija.metodo()  # Salida: "Método de la clase hija"
```

#### Buenas prácticas y uso:

- El polimorfismo de clase de herencia en Python permite escribir un código más modular y extensible, ya que se pueden definir clases que comparten un comportamiento común pero que pueden tener variaciones en ciertos métodos.
- Al utilizar el polimorfismo, se aprovecha la flexibilidad y el dinamismo que ofrece Python como lenguaje orientado a objetos.
- Es importante documentar adecuadamente las clases y métodos para facilitar su comprensión y mantenimiento en el futuro.

El polimorfismo de clase de herencia en Python es una herramienta poderosa que permite crear jerarquías de clases con comportamientos distintos, favoreciendo la reutilización de código y la simplificación de la estructura del programa.