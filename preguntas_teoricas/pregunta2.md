## **¿Qué método se ejecuta automáticamente cuando se crea una instancia de una clase?**

En Python, el método `__init__` se ejecuta automáticamente cuando se crea una instancia de una clase. Este método es conocido como el "constructor" de la clase y se utiliza para inicializar los atributos de la instancia. 

### La sintaxis

La sintaxis del método `__init__` en Python es la siguiente:

```python
class MiClase:
    def __init__(self, parametroA, parametroB):
        self.atributo1 = parametroA
        self.atributo2 = parametroB
```

En este ejemplo, estamos definiendo una clase llamada MiClase con un método `__init__` que toma dos parámetros y asigna esos parámetros a los atributos `atributoA` y `atributoB` de la instancia.

### Buenas prácticas

Es una buena práctica utilizar el método `__init__` para inicializar todos los atributos necesarios de la clase y establecer sus valores iniciales. Esto ayuda a mantener un código limpio y legible, así como a garantizar que las instancias de la clase estén correctamente inicializadas.

```python
mi_instancia = MiClase("valorA", "valorB")
print(mi_instancia.atributoA) # salida: valorA
print(mi_instancia.atributoB) # salida: valorB
```

En este ejemplo, creamos una instancia de la clase `MiClase` utilizando el método `__init__ `y luego imprimimos los valores de los atributos `atributoA` y `atributoB`.

El método `__init__` en Python es una parte fundamental de la programación orientada a objetos y se utiliza para garantizar que las instancias de una clase estén correctamente inicializadas y listas para su uso.