## **¿Cuáles son los tres verbos de API?**

En Python, los tres verbos principales para realizar solicitudes a una API son GET, POST y DELETE.

### GET

Este verbo se utiliza para recuperar datos de una API. Se utiliza cuando queremos obtener información de un recurso específico.

#### Sintaxis

La sintaxis básica para hacer una solicitud GET en Python con la biblioteca requests es la siguiente:

```python
import requests

response = requests.get('https://api.example.com/data')
print(response.json())
```

En este ejemplo, estamos haciendo una solicitud GET a `https://api.example.com/data` y luego imprimimos la respuesta en formato JSON.

#### Buenas prácticas

Es importante recordar algunas buenas prácticas al hacer solicitudes GET en una API, como manejar posibles errores de conexión o respuesta del servidor, validar la respuesta recibida antes de procesarla y utilizar parámetros de consulta si es necesario.

```python
import requests

response = requests.get('https://api.example.com/data', params={'key': 'value'})
print(response.json())
```

Además, es recomendable documentar claramente cómo usar la API y qué datos se pueden esperar en la respuesta a una solicitud GET para facilitar el uso por parte de otros desarrolladores.

El verbo GET en Python es una forma efectiva de obtener datos de una API y puede ser fácilmente implementado con bibliotecas como requests. Es importante seguir buenas prácticas y documentar cuidadosamente la API para garantizar su uso eficiente y correcto.

## POST

El verbo POST de una API en Python se utiliza para enviar datos a un servidor para crear o actualizar un recurso. Este verbo se utiliza comúnmente en solicitudes de formularios en línea, envío de mensajes o cualquier tipo de operación que requiera enviar información al servidor.

#### Sintaxis

La sintaxis básica para realizar una solicitud POST en Python usando el módulo `requests` es la siguiente:

```python
import requests

url = 'https://ejemplo.com/api/recurso'
datos = {'campo1': 'valor1', 'campo2': 'valor2'}

respuesta = requests.post(url, data=datos)
```

En este ejemplo, se está enviando una solicitud POST a la URL `https://ejemplo.com/api/recurso` con los datos `campo1` y `campo2` y sus respectivos valores.

#### Buenas prácticas

1. Asegurarse de que la URL a la que se envía la solicitud sea segura (utilizando HTTPS en lugar de HTTP).
1. Validar los datos antes de enviarlos al servidor para prevenir posibles errores o vulnerabilidades en la aplicación.
1. Utilizar la librería `requests` de Python para realizar las solicitudes POST, ya que proporciona una forma sencilla y eficiente de interactuar con APIs.

Algunos ejemplos de situaciones en las que se podría utilizar el verbo POST en una API en Python incluyen crear un usuario en una base de datos, enviar un mensaje a un grupo de usuarios o realizar una compra en línea.

El verbo POST en una API en Python es una herramienta fundamental para enviar datos al servidor y realizar operaciones que requieran esta acción. Es importante seguir buenas prácticas al utilizarlo y aprovechar las funcionalidades que ofrece la librería `requests` para optimizar el proceso de envío de datos.

### DELETE

El verbo DELETE en una API en Python se utiliza para eliminar un recurso específico del servidor. Es una operación CRUD (Create, Read, Update, Delete) que permite al cliente eliminar datos de la base de datos del servidor.

#### Sintaxis

La sintaxis para realizar una solicitud DELETE en Python generalmente se hace a través de la biblioteca requests. Aquí tienes un ejemplo de cómo se vería una solicitud DELETE en Python:

```python
import requests

url = 'https://api.ejemplo.com/recurso/1'
response = requests.delete(url)

print(response.status_code) # Debería devolver 200 si la eliminación fue exitosa
```

Es importante mencionar que el recurso que se quiere eliminar debe ser especificado en la URL de la solicitud DELETE.

#### Buenas prácticas

1. Verificar que el usuario tiene los permisos necesarios para eliminar el recurso.
1. Confirmar la eliminación con un mensaje de éxito o error para informar al cliente.
1. Implementar medidas de seguridad para prevenir la eliminación accidental de datos importantes.

En cuanto a por qué se utiliza el verbo DELETE en una API, es fundamental para mantener la integridad de los datos y permitir a los clientes gestionar los recursos de manera eficiente. Al eliminar un recurso, se asegura que los datos no estén desactualizados o almacenados innecesariamente en el servidor.

En resumen, el verbo DELETE en una API en Python es una herramienta poderosa para gestionar recursos y mantener la base de datos actualizada. Es importante utilizarlo con precaución y seguir las buenas prácticas mencionadas para garantizar la seguridad y la integridad de los datos. ¡Espero que esta información te sea útil!

