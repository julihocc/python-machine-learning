# Encapsulamiento

El encapsulamiento es un principio de la programación orientada a objetos que permite ocultar los detalles de implementación de una clase y exponer solo una interfaz pública para interactuar con ella. En Python, se utiliza el prefijo de doble guion bajo (`__`) para marcar un atributo o método como privado y que solo pueda ser accedido desde dentro de la clase.

Por ejemplo, la siguiente clase define un atributo privado llamado `_nombre` y un método público llamado `get_nombre()` que devuelve el valor de ese atributo:

```python
class Persona:
    def __init__(self, nombre):
        self._nombre = nombre

    def get_nombre(self):
        return self._nombre
```

Para acceder al atributo `_nombre` desde fuera de la clase, debemos utilizar el método `get_nombre()`. De esta manera, estamos asegurando que el valor del atributo no pueda ser modificado accidentalmente por código que no pertenece a la clase.

El encapsulamiento tiene varias ventajas, entre las que se incluyen:

* **Mejora la legibilidad y mantenibilidad del código.** Al ocultar los detalles de implementación, el código es más fácil de entender y mantener.
* **Reduce el riesgo de errores.** Al limitar el acceso a los atributos y métodos, es menos probable que se produzcan errores debido a una modificación accidental.
* **Permite la reutilización del código.** Las clases encapsuladas son más fáciles de reutilizar en otros proyectos.

En Python, el encapsulamiento es una convención, no un requisito del lenguaje. Sin embargo, es una buena práctica utilizar el encapsulamiento para mejorar la calidad del código.

Aquí hay algunos ejemplos de cómo utilizar el encapsulamiento en Python:

* **Para ocultar información sensible.** Por ejemplo, podemos utilizar el encapsulamiento para ocultar el número de cuenta bancaria o la dirección de correo electrónico de un usuario.
* **Para proteger datos de acceso no autorizado.** Por ejemplo, podemos utilizar el encapsulamiento para proteger los datos de un usuario de un ataque de inyección SQL.
* **Para organizar el código de forma lógica.** Podemos utilizar el encapsulamiento para agrupar los atributos y métodos relacionados en una clase.

El encapsulamiento es una herramienta poderosa que puede ayudarnos a escribir código más seguro y eficiente.

## Atributos privados 
En Python, no existen atributos privados de forma nativa. Sin embargo, es posible crear atributos privados utilizando el prefijo de doble guion bajo (`__`). Este prefijo no impide que el atributo sea accedido desde fuera de la clase, pero sí dificulta su acceso.

En Python 3.8, se introdujo una nueva característica llamada name mangling que hace que sea aún más difícil acceder a los atributos privados desde fuera de la clase. Con name mangling, el prefijo de doble guion bajo se reemplaza por un nombre generado automáticamente que es único para la clase.

Por ejemplo, la siguiente clase define un atributo privado llamado `_nombre`:

```python
class Persona:
    def __init__(self, nombre):
        self._nombre = nombre
```

Para acceder al atributo `_nombre` desde fuera de la clase, podemos utilizar el operador `__getattr__()`. Este operador permite a la clase interceptar las solicitudes de acceso a atributos que no existen.

```python
>>> persona = Persona("Juan")
>>> persona._nombre
AttributeError: 'Persona' object has no attribute '__nombre'
>>> persona.__getattr__("_nombre")
'Juan'
```

Sin embargo, este método es poco práctico para acceder a los atributos privados de forma habitual.

Una mejor práctica es utilizar un método público para acceder al atributo privado. Este método puede proporcionar una interfaz controlada para acceder al atributo.

```python
class Persona:
    def __init__(self, nombre):
        self._nombre = nombre

    def get_nombre(self):
        return self._nombre

>>> persona = Persona("Juan")
>>> persona.get_nombre()
'Juan'
```

De esta manera, estamos asegurando que el valor del atributo solo pueda ser modificado por código que pertenece a la clase.

# Getters y setter 
El decorador `@property` es una forma conveniente de crear propiedades en Python. Una propiedad es una variable que puede ser accedida como un atributo, pero que tiene un comportamiento especial al ser asignada o accedida.

Para utilizar el decorador `@property`, debemos definir un método que devuelva el valor de la propiedad. El decorador `@property` creará automáticamente los métodos `getter` y `setter` para la propiedad.

Por ejemplo, la siguiente clase define una propiedad llamada `nombre` que devuelve el valor del atributo privado `_nombre`:

```python
class Persona:
    def __init__(self, nombre):
        self._nombre = nombre

    @property
    def nombre(self):
        return self._nombre

>>> persona = Persona("Juan")
>>> persona.nombre
'Juan'
```

El método `getter` se llama automáticamente cuando se accede a la propiedad. El método `setter` se llama automáticamente cuando se asigna un valor a la propiedad.

El decorador `@property` tiene tres parámetros opcionales:

* `fget`: El método que devuelve el valor de la propiedad.
* `fset`: El método que asigna un valor a la propiedad.
* `fdel`: El método que elimina la propiedad.

Por ejemplo, la siguiente clase define una propiedad llamada `edad` que permite validar el valor asignado:

```python
class Persona:
    def __init__(self, nombre, edad):
        self._nombre = nombre
        self._edad = edad

    @property
    def edad(self):
        return self._edad

    @edad.setter
    def edad(self, edad):
        if edad < 18:
            raise ValueError("La edad debe ser mayor o igual a 18")
        self._edad = edad

>>> persona = Persona("Juan", 18)
>>> persona.edad
18
>>> persona.edad = 17
Traceback (most recent call last):
...
ValueError: La edad debe ser mayor o igual a 18
```

En este ejemplo, el método `setter` comprueba que el valor asignado a la propiedad `edad` es mayor o igual a 18. Si el valor no es válido, se lanza una excepción `ValueError`.

El decorador `@property` es una herramienta poderosa que puede ayudarnos a escribir código más conciso y legible.
