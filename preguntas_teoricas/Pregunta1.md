## **¿Para qué usamos Clases en Python?**

Las clases en Python son una herramienta fundamental para la programación orientada a objetos. Permiten organizar y estructurar nuestro código de una manera más clara y modular, lo que facilita su mantenimiento y reutilización.

Una clase en Python es como un plano o una plantilla que define la estructura y comportamiento de un objeto. Dentro de una clase podemos definir atributos (variables) y métodos (funciones) que representan las características y acciones que el objeto puede realizar.

### Sintaxis
La sintaxis para definir una clase en Python es la siguiente:
```python
class MiClase:
    def __init__(self, parametro):
        self.parametro = parametro

    def metodo(self):
        # código del método
```
En este ejemplo, la clase `MiClase` tiene un constructor `__init__` que inicializa un parámetro y un método `metodo`. Para crear un objeto de esta clase, simplemente llamamos al constructor y asignamos el objeto resultante a una variable.

### Ejemplo

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
    
    def saludar(self):
        print(f'Hola, me llamo {self.nombre} y tengo {self.edad} años.')

persona1 = Persona("Ivan", 27)
persona1.saludar()
```
En el ejemplo anterior, se define una clase `Persona` con un método `saludar` que imprime un mensaje con el nombre y la edad de la persona. Luego se crea un objeto `persona1` a partir de la clase `Persona` y se llama al método `saludar` del objeto.

### Buenas prácticas

_Algunas buenas prácticas al trabajar con clases en Python son:_

* Seguir la convención de nombres PEP 8 para nombrar las clases y los métodos.
* Documentar el propósito de la clase y los métodos utilizando docstrings.
* Seguir el principio de encapsulamiento y no acceder a los atributos de la clase directamente desde fuera de la misma.
* Utilizar la herencia de forma consciente y jerárquica.
* Mantener las clases simples y cohesivas, con una única responsabilidad.

### Por qué usar clases

_Reutilización de código_: Las clases permiten definir estructuras de código que se pueden reutilizar en diferentes partes de un programa.
 ```python
 #### Ejemplo:
 class Vehiculo:
     def __init__(self, marca, modelo):
         self.marca = marca
         self.modelo = modelo
         
     def info(self):
         return f'{self.marca} {self.modelo}'

 class Coche(Vehiculo):
     def __init__(self, marca, modelo, color):
         super().__init__(marca, modelo)
         self.color = color
         
     def info(self):
         return f'{super().info()} de color {self.color}'

 coche = Coche('Ford', 'Fiesta', 'Azul')
 print(coche.info())
 ```

_Modularidad:_ Las clases facilitan la organización del código en módulos y permiten separar la lógica del programa en distintas partes, lo que hace que sea más fácil de entender y mantener.

_Abstracción:_ Las clases permiten representar entidades del mundo real o conceptos abstractos de una manera más efectiva, facilitando la comprensión y el diseño del programa.

_Encapsulación:_ Las clases permiten encapsular datos y funciones relacionadas en un solo objeto, lo que ayuda a evitar la manipulación no deseada de los datos y a mantener la integridad del programa.

_Herencia:_ Las clases en Python permiten la herencia, lo que significa que una clase puede heredar atributos y métodos de otra clase, lo que facilita la reutilización y extensión del código.


