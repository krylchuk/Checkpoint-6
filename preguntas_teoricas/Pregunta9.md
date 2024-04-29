## **¿Qué es un decorador de python?**

Un decorador en Python es una función que toma como argumento otra función y devuelve una nueva función modificada. Los decoradores son una característica poderosa y flexible de Python que permite agregar funcionalidades a las funciones existentes sin modificar su código original.

### Sintaxis
La sintaxis básica para definir un decorador es la siguiente:
```python
def mi_decorador(funcion):
    def nueva_funcion():
        # código adicional
        resultado = funcion()
        # código adicional
        return resultado
    return nueva_funcion
```

Para aplicar un decorador a una función, simplemente se coloca el nombre del decorador precedido por el caracter "@" justo encima de la definición de la función a decorar:
```python
@mi_decorador
def mi_funcion():
    # código de la función
```

### Ejemplo
```python
def imprimir_mensaje(funcion):
    def decorador():
        print("Se está ejecutando la función:")
        funcion()
        print("La función ha finalizado.")
    return decorador

@imprimir_mensaje
def saludar():
    print("Hola, mundo!")

saludar()
```

### ¿Por qué se utiliza un decorador?
Los decoradores son útiles para separar la lógica de una función de las tareas adicionales que pueden necesitarse, como la validación de datos, el registro de eventos o la medición del tiempo de ejecución. Esto ayuda a mantener el código limpio y legible, además de fomentar la reutilización de código.

### Buenas prácticas
* Los decoradores son útiles para reutilizar código y aplicar funcionalidades comunes a múltiples funciones.
* Mejoran la legibilidad del código al separar las preocupaciones y modularizar el comportamiento.
* Permiten encapsular lógica repetitiva o de uso frecuente de una manera elegante y sencilla.
* Ayudan a mantener el código limpio y organizado al evitar la repetición de código.

Los decoradores son una poderosa herramienta en Python que permite añadir funcionalidades adicionales a las funciones de forma sencilla y flexible. Su uso puede mejorar la organización del código y facilitar la incorporación de nuevas características sin afectar la funcionalidad original.
