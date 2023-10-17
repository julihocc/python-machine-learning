## **Funciones en Python**

### **1. Introducción a las funciones**

- Una función es un bloque de código organizado y reutilizable que se utiliza para realizar una única acción relacionada.
- Las funciones proporcionan una mejor modularidad para su aplicación y un alto grado de reutilización de código.

### **2. Definición de una función**

- En Python, una función se define usando la palabra clave `def` seguida del nombre de la función y paréntesis `()`.

```python
def nombre_funcion():
    # Código de la función
```

### **3. Llamada a una función**

- Una vez que se define una función, se puede llamar desde otra función, programa o incluso desde la terminal.

```python
nombre_funcion()
```

### **4. Parámetros y argumentos**

- Los parámetros son valores que puedes pasar a una función para que la función los utilice.
- Los parámetros se especifican después del nombre de la función, dentro de los paréntesis.

```python
def saludo(nombre):
    print("Hola, " + nombre)

saludo("Ana")  # Salida: Hola, Ana
```

### **5. Valores de retorno**

- Una función puede devolver un valor usando la instrucción `return`.

```python
def suma(a, b):
    return a + b

resultado = suma(3, 4)  # resultado es 7
```

### **6. Variables locales y globales**

- Las variables definidas dentro de una función tienen un alcance local, lo que significa que solo pueden ser accedidas dentro de esa función.
- Las variables definidas fuera de cualquier función tienen un alcance global.

### **7. Funciones anónimas (lambda)**

- Python permite la creación de funciones anónimas (es decir, funciones que no se declaran con la palabra clave `def` estándar) usando la palabra clave `lambda`.
- Las funciones lambda pueden tener cualquier número de argumentos, pero solo una expresión.

```python
multiplica = lambda x, y: x * y
print(multiplica(5, 3))  # Salida: 15
```

### **8. Documentación de funciones**

- Es una buena práctica documentar tus funciones para que otros desarrolladores (o tú mismo en el futuro) puedan entender qué hace la función.
- En Python, esto se hace usando cadenas de documentación (docstrings).

```python
def suma(a, b):
    """
    Esta función suma dos números y devuelve el resultado.
    """
    return a + b
```
