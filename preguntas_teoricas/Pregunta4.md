## **¿Es MongoDB una base de datos SQL o NoSQL?**

MongoDB es una base de datos NoSQL en python. NoSQL significa "Not Only SQL" y se refiere a un enfoque de bases de datos que no utiliza el lenguaje de consulta estructurado (SQL) para manipular datos. En lugar de tener tablas como en las bases de datos SQL, MongoDB almacena datos en colecciones de documentos JSON.

MongoDB es una base de datos muy flexible y escalable que se adapta bien a aplicaciones modernas que necesitan manejar grandes volúmenes de datos y necesitan cambios rápidos en la estructura de los datos. Permite la indexación de campos, la búsqueda rápida de datos y la capacidad de escalar horizontalmente a través de múltiples servidores.

En Python, podemos interactuar con MongoDB utilizando la biblioteca oficial de MongoDB llamada "pymongo". Aquí hay un ejemplo básico de cómo conectarse a una base de datos MongoDB y realizar algunas operaciones:

```python
import pymongo

# Conectarse a la base de datos
client = pymongo.MongoClient("mongodb://localhost:27017/")
db = client["mi_base_de_datos"]

# Crear una colección dentro de la base de datos
coleccion = db["mi_coleccion"]

# Insertar un documento en la colección
documento = {"nombre": "Ivan", "edad": 27}
coleccion.insert_one(documento)

# Buscar un documento en la colección
resultado = coleccion.find_one({"nombre": "Ivan"})
print(resultado)
```

### Buenas prácticas

Es importante diseñar la estructura de la base de datos en función de las consultas que se realizarán con mayor frecuencia. También es importante indexar los campos que se utilizarán para búsquedas frecuentes, ya que esto mejorará el rendimiento de las consultas.

MongoDB se utiliza comúnmente en aplicaciones web, análisis de datos y aplicaciones móviles debido a su flexibilidad y escalabilidad. También es una buena opción para aplicaciones que necesitan manejar datos semi-estructurados o no estructurados.
