# Variables

En el contexto de programación y, específicamente, en Python, una variable es un nombre que se refiere a un valor o a un objeto en memoria. Las variables se utilizan para almacenar información que se puede referenciar y manipular en un programa.

Aquí hay algunas características y detalles sobre las variables en Python:

1. **Asignación**: En Python, se utiliza el signo `=` para asignar un valor a una variable. Por ejemplo:
   ```python
   x = 5
   nombre = "Juan"
   ```

2. **Tipos Dinámicos**: A diferencia de otros lenguajes de programación, no necesitas declarar el tipo de dato de una variable en Python. El tipo de dato se determina dinámicamente en tiempo de ejecución. Por ejemplo:
   ```python
   x = 5        # x es un entero
   x = "Hola"   # ahora x es una cadena
   ```

3. **Nombres de Variables**: Los nombres de las variables en Python pueden contener letras, números y guiones bajos, pero deben comenzar con una letra o un guión bajo. No pueden comenzar con un número.

4. **Sensibles a Mayúsculas y Minúsculas**: Las variables en Python son sensibles al caso, lo que significa que `nombre`, `Nombre` y `NOMBRE` serían tres variables diferentes.

5. **Referencia**: Cuando asignas un objeto a una variable, en realidad estás asignando una referencia al objeto, no una copia del objeto. Esto es especialmente relevante cuando trabajas con objetos mutables, como listas.

6. **Eliminación de Variables**: Puedes eliminar una variable usando la palabra clave `del`. Por ejemplo:
   ```python
   del x
   ```

En resumen, una variable en Python es como una etiqueta que se pega a un objeto en memoria, permitiéndote acceder, modificar o referenciar ese objeto en tu programa.

# Tipos de variables

En Python, hay varios tipos de datos básicos que se pueden asignar a las variables. Estos son los más comunes:

1. **Integers (`int`)**: Representan números enteros, ya sean positivos o negativos.
   ```python
   x = 5
   y = -3
   ```

2. **Floating Point (`float`)**: Representan números reales (es decir, números con decimales).
   ```python
   a = 3.14
   b = -0.001
   ```

3. **Strings (`str`)**: Representan secuencias de caracteres.
   ```python
   nombre = "Juan"
   saludo = 'Hola, ¿cómo estás?'
   ```

4. **Booleans (`bool`)**: Representan valores de verdad, es decir, `True` o `False`.
   ```python
   es_verdadero = True
   es_falso = False
   ```

5. **Complex**: Representan números complejos, que tienen una parte real y una parte imaginaria.
   ```python
   z = 1 + 2j
   ```

6. **Bytes**: Representan secuencias de bytes, que son similares a las cadenas, pero se utilizan para representar datos binarios.
   ```python
   data = b'Hola'
   ```

7. **NoneType (`None`)**: Representa la ausencia de valor o un valor nulo. Es un tipo especial en Python.
   ```python
   vacio = None
   ```

Además de estos tipos básicos, Python también ofrece tipos de datos compuestos o estructuras de datos, como listas, tuplas, conjuntos y diccionarios. Estos permiten almacenar colecciones de valores:

- **Listas (`list`)**: Colecciones ordenadas y mutables.
  ```python
  frutas = ["manzana", "plátano", "cereza"]
  ```

- **Tuplas (`tuple`)**: Colecciones ordenadas e inmutables.
  ```python
  coordenadas = (4, 5)
  ```

- **Conjuntos (`set`)**: Colecciones no ordenadas de elementos únicos.
  ```python
  s = {1, 2, 3, 3}
  ```

- **Diccionarios (`dict`)**: Colecciones no ordenadas de pares clave-valor.
  ```python
  persona = {"nombre": "Juan", "edad": 30}
  ```

Estos son los tipos de datos básicos y algunas de las estructuras de datos más comunes en Python. Es importante tener en cuenta que Python es un lenguaje de tipado dinámico, lo que significa que el tipo de una variable se determina en tiempo de ejecución y puede cambiar a medida que se ejecuta el programa.
