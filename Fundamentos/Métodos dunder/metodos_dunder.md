Los métodos dunder, también conocidos como métodos mágicos, son métodos especiales que tienen un nombre que comienza y termina con dos guiones bajos (dunder). Estos métodos son utilizados por el intérprete de Python para realizar operaciones comunes en los objetos.

Los métodos dunder se utilizan para:

* **Sobrecarga de operadores:** Los métodos dunder se utilizan para sobrecargar los operadores matemáticos y lógicos. Por ejemplo, el método __add__() se utiliza para sobrecargar el operador de suma (+).
* **Clase de representación:** Los métodos dunder __str__() y __repr__() se utilizan para representar un objeto de una manera legible para los humanos.
* **Comparación de objetos:** Los métodos dunder __eq__(), __ne__(), __lt__(), __le__(), __gt__() y __ge__() se utilizan para comparar dos objetos.
* **Coerción de tipos:** Los métodos dunder __int__(), __float__(), __complex__(), __str__(), __bytes__(), __bool__() y __hash__() se utilizan para convertir un objeto a un tipo diferente.

**Ejemplo de un método dunder**

La siguiente clase define un objeto `Persona` con un método dunder __str__():

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def __str__(self):
        return "{} ({})".format(self.nombre, self.edad)


persona = Persona("Juan", 20)

print(persona)
```

Este código imprime el siguiente mensaje:

```
Juan (20)
```

**Lista de métodos dunder**

Los métodos dunder más comunes son:

* **__init__()**: Constructor del objeto.
* **__str__()**: Representa el objeto de una manera legible para los humanos.
* **__repr__()**: Representa el objeto de una manera legible para los programadores.
* **__eq__()**: Compara dos objetos para ver si son iguales.
* **__ne__()**: Compara dos objetos para ver si son diferentes.
* **__lt__()**: Compara dos objetos para ver si el primer objeto es menor que el segundo.
* **__le__()**: Compara dos objetos para ver si el primer objeto es menor o igual que el segundo.
* **__gt__()**: Compara dos objetos para ver si el primer objeto es mayor que el segundo.
* **__ge__()**: Compara dos objetos para ver si el primer objeto es mayor o igual que el segundo.
* **__add__()**: Sobrecarga el operador de suma (+).
* **__sub__()**: Sobrecarga el operador de resta (-).
* **__mul__()**: Sobrecarga el operador de multiplicación (*).
* **__div__()**: Sobrecarga el operador de división (/).
* **__mod__()**: Sobrecarga el operador de módulo (%).
* **__pow__()**: Sobrecarga el operador de potenciación (**).
* **__and__()**: Sobrecarga el operador lógico y (and).
* **__or__()**: Sobrecarga el operador lógico o (or).
* **__xor__()**: Sobrecarga el operador lógico exclusivo o (xor).
* **__not__()**: Sobrecarga el operador lógico no (not).
* **__int__()**: Convierte el objeto a un entero.
* **__float__()**: Convierte el objeto a un número flotante.
* **__complex__()**: Convierte el objeto a un número complejo.
* **__str__()**: Convierte el objeto a una cadena de caracteres.
* **__bytes__()**: Convierte el objeto a una secuencia de bytes.
* **__bool__()**: Devuelve True si el objeto es verdadero, False si es falso.
* **__hash__()**: Devuelve un hash del objeto.

Los métodos dunder son una parte importante de la programación en Python. Se utilizan para realizar operaciones comunes en los objetos y para sobrecargar operadores y tipos.
