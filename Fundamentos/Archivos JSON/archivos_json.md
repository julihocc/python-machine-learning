# Archivos JSON
Los archivos JSON son archivos de texto que contienen datos estructurados en un formato fácil de leer y escribir. El formato JSON es un subconjunto de la sintaxis de objetos literales de JavaScript, pero se considera un formato independiente del lenguaje.

Los archivos JSON se utilizan para almacenar y transmitir datos entre aplicaciones. Son un formato popular para el intercambio de datos entre aplicaciones web y servidores, ya que son fáciles de generar y parsear.

Los archivos JSON se suelen utilizar para almacenar datos como:

* Listas de datos
* Objetos complejos
* Datos de configuración
* Datos de registro

Los archivos JSON tienen una estructura simple que consta de pares clave-valor. Las claves son cadenas de texto que identifican los valores. Los valores pueden ser cadenas de texto, números, booleanos, objetos o arrays.

Un ejemplo de un archivo JSON es el siguiente:

```json
{
  "nombre": "Juan Pérez",
  "edad": 30,
  "hobbies": ["deporte", "música", "lectura"]
}
```

Este archivo JSON representa un objeto con tres propiedades: nombre, edad y hobbies. La propiedad nombre tiene un valor de cadena, la propiedad edad tiene un valor numérico y la propiedad hobbies tiene un array de valores de cadena.

Los archivos JSON se pueden abrir y editar con cualquier editor de texto. También existen herramientas y bibliotecas para trabajar con archivos JSON en varios lenguajes de programación.

**Ventajas de los archivos JSON**

Los archivos JSON ofrecen las siguientes ventajas:

* Son fáciles de leer y escribir
* Son independientes del lenguaje
* Son compactos y eficientes
* Son fáciles de transmitir

**Desventajas de los archivos JSON**

Los archivos JSON tienen las siguientes desventajas:

* No son tan expresivos como otros formatos de datos, como XML
* Pueden ser propensos a errores si no se utilizan correctamente

**Usos de los archivos JSON**

Los archivos JSON se utilizan en una amplia gama de aplicaciones, incluyendo:

* Aplicaciones web
* Aplicaciones móviles
* Aplicaciones de escritorio
* Servicios web
* Bases de datos

**Conclusión**

Los archivos JSON son un formato de datos popular que se utiliza para almacenar y transmitir datos entre aplicaciones. Son un formato fácil de leer y escribir, independiente del lenguaje y eficiente.

## Librería `request`
La librería requests de Python es una biblioteca que facilita la realización de peticiones HTTP. Se puede utilizar para realizar peticiones a sitios web, API, etc.

**Instalación**

Para instalar la librería requests en Python, puedes utilizar el siguiente comando:

```
pip install requests
```

**Importación**

Una vez instalada, la librería se puede importar en tu código de la siguiente manera:

```python
import requests
```

**Realización de peticiones**

La librería requests proporciona una función llamada `get()` para realizar peticiones HTTP GET. Esta función toma como argumento la URL de la petición. Por ejemplo, para realizar una petición a la página principal de Google, utilizaríamos el siguiente código:

```python
response = requests.get('https://www.google.com')
```

Esta función devolverá un objeto de tipo `requests.Response`. Este objeto contiene información sobre la petición, como el código de estado, el encabezado y el cuerpo de la respuesta.

Para obtener el código de estado de la respuesta, podemos utilizar el atributo `status_code` del objeto `Response`:

```python
response.status_code
```

Para obtener el encabezado de la respuesta, podemos utilizar el atributo `headers` del objeto `Response`:

```python
response.headers
```

Para obtener el cuerpo de la respuesta, podemos utilizar el método `text()` del objeto `Response`:

```python
response.text
```

**Peticiones con parámetros**

Las peticiones HTTP GET también pueden incluir parámetros. Para ello, podemos utilizar la función `params()` de la clase `requests.Request`. Por ejemplo, para realizar una búsqueda en Google, utilizaríamos el siguiente código:

```python
response = requests.get('https://www.google.com/search', params={'q': 'Python'})
```

Este código enviará la siguiente petición HTTP:

```
GET /search?q=Python HTTP/1.1
Host: www.google.com
```

**Peticiones POST**

La librería requests también proporciona una función llamada `post()` para realizar peticiones HTTP POST. Esta función toma como argumento un diccionario que contiene los datos que se quieren enviar en el cuerpo de la petición. Por ejemplo, para realizar una solicitud de registro en un sitio web, utilizaríamos el siguiente código:

```python
data = {
    'username': 'user1',
    'password': 'secret'
}

response = requests.post('https://example.com/register', data=data)
```

Este código enviará la siguiente petición HTTP:

```
POST /register HTTP/1.1
Host: example.com
Content-Type: application/json

{
    "username": "user1",
    "password": "secret"
}
```

**Peticiones con autenticación**

La librería requests también proporciona soporte para peticiones con autenticación. Para realizar una petición con autenticación básica, podemos utilizar la función `auth()` de la clase `requests.Request`. Por ejemplo, para realizar una petición a un servidor FTP, utilizaríamos el siguiente código:

```python
auth = ('user', 'password')

response = requests.get('ftp://example.com/', auth=auth)
```

Este código enviará la siguiente petición HTTP:

```
GET / HTTP/1.1
Host: example.com
Authorization: Basic dXNlcm5hbWU6cGFzc3dvcmQ=
```

**Peticiones con cookies**

La librería requests también proporciona soporte para peticiones con cookies. Para realizar una petición con cookies, podemos utilizar el método `cookies()` de la clase `requests.Session`. Por ejemplo, para realizar una petición a un sitio web que requiere que el usuario esté registrado, utilizaríamos el siguiente código:

```python
session = requests.Session()

# Obtener las cookies del navegador
cookies = requests.get('https://example.com/').cookies

# Utilizar las cookies para realizar una petición
response = session.get('https://example.com/private', cookies=cookies)
```

Este código enviará la siguiente petición HTTP:

```
GET /private HTTP/1.1
Host: example.com
Cookie: ...
```

**Más información**

Para obtener más información sobre la librería requests, puedes consultar la documentación oficial: https://requests.readthedocs.io/en/master/.

**Ejemplos**

A continuación, se muestran algunos ejemplos de uso de la librería requests:
