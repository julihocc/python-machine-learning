# Diccionarios 

En Python, los diccionarios son una estructura de datos que almacenan datos en pares de clave-valor. Las claves deben ser únicas y pueden ser de cualquier tipo de dato inmutable, como cadenas, números o tuplas. Los valores pueden ser de cualquier tipo de dato, incluyendo diccionarios anidados.

Los diccionarios se pueden crear usando corchetes {} y separando cada par clave-valor con una coma. Por ejemplo:

```python
diccionario = {
    "nombre": "Juan",
    "edad": 25,
    "ciudad": "Madrid"
}
```

También se pueden crear usando la función `dict()`. Por ejemplo:

```python
diccionario = dict(nombre="Juan", edad=25, ciudad="Madrid")
```

Para acceder a un valor de un diccionario, se utiliza la clave correspondiente. Por ejemplo:

```python
print(diccionario["nombre"])
```

Esto imprimirá la cadena "Juan".

Los diccionarios se pueden modificar agregando, eliminando o modificando elementos. Para agregar un elemento, se utiliza el operador `update()`. Por ejemplo:

```python
diccionario["teléfono"] = "666-123-456"
```

Esto agregará un elemento con la clave "teléfono" y el valor "666-123-456" al diccionario.

Para eliminar un elemento, se utiliza la función `pop()`. Por ejemplo:

```python
diccionario.pop("edad")
```

Esto eliminará el elemento con la clave "edad" del diccionario.

Para modificar un elemento, se utiliza la sintaxis de asignación. Por ejemplo:

```python
diccionario["nombre"] = "María"
```

Esto modificará el valor del elemento con la clave "nombre" a "María".

Los diccionarios son una estructura de datos muy versátil que se puede utilizar para almacenar datos de una amplia variedad de formas. Son útiles para almacenar datos que están relacionados entre sí, como los datos de una persona o los datos de un producto.

Aquí hay algunos ejemplos de cómo se pueden usar los diccionarios en Python:

* Almacenar los datos de un usuario, como el nombre, la edad y la dirección.
* Almacenar los datos de un producto, como el nombre, el precio y la descripción.
* Almacenar los datos de un evento, como la fecha, la hora y el lugar.
* Almacenar los datos de una lista de tareas, como la tarea, la prioridad y la fecha límite.

Los diccionarios son una herramienta poderosa que puede ayudar a los programadores a organizar y almacenar datos de una manera eficiente.

## Ciclo `for`
Para recorrer un diccionario con el ciclo for en Python, se puede utilizar la sintaxis `for clave in diccionario:`. Esto iterará sobre todas las claves del diccionario y asignará cada clave a la variable `clave`.

Por ejemplo, el siguiente código recorre un diccionario que contiene información sobre una persona:

```python
diccionario = {
    "nombre": "Juan",
    "edad": 25,
    "ciudad": "Madrid"
}

for clave in diccionario:
    print(clave, diccionario[clave])
```

Esto imprimirá lo siguiente:

```
nombre Juan
edad 25
ciudad Madrid
```

También se puede utilizar la sintaxis `for valor in diccionario.values()` para iterar sobre todos los valores del diccionario. Esto asignará cada valor a la variable `valor`.

Por ejemplo, el siguiente código recorre un diccionario que contiene información sobre una persona:

```python
diccionario = {
    "nombre": "Juan",
    "edad": 25,
    "ciudad": "Madrid"
}

for valor in diccionario.values():
    print(valor)
```

Esto imprimirá lo siguiente:

```
Juan
25
Madrid
```

Finalmente, se puede utilizar la sintaxis `for clave, valor in diccionario.items()` para iterar sobre todos los pares clave-valor del diccionario. Esto asignará cada par clave-valor a la variable `clave` y `valor`, respectivamente.

Por ejemplo, el siguiente código recorre un diccionario que contiene información sobre una persona:

```python
diccionario = {
    "nombre": "Juan",
    "edad": 25,
    "ciudad": "Madrid"
}

for clave, valor in diccionario.items():
    print(clave, valor)
```

Esto imprimirá lo siguiente:

```
nombre Juan
edad 25
ciudad Madrid
```

La sintaxis que se utilice dependerá de las necesidades del programa.
