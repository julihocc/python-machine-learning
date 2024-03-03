---
marp: true
theme: uncover
author: Prof. Juliho Castillo Colmenares Ph.D.
title: Cálculo
description: Curso propedéutico de Computación
---

# Tutorial de SciPy
### Una introducción a las herramientas esenciales para cálculos matemáticos

---

# Índice

1. Introducción a SciPy
2. Derivación con SciPy
3. Resolución de Ecuaciones Diferenciales
4. Cálculo del Gradiente
5. Integración Numérica
6. Encontrar Raíces de Funciones
7. Derivadas Parciales

---

# 1. Introducción a SciPy

SciPy es una biblioteca de Python que se utiliza para cálculos matemáticos de alto nivel. Contiene módulos para optimización, álgebra lineal, integración, interpolación, y muchas otras tareas.

---

# 2. Derivación con SciPy

Para derivar una función en SciPy, puedes usar:

- **scipy.derivative()**: Esta función te permite calcular la derivada de una función en un punto dado.

---

```python
from scipy.misc import derivative

def f(x):
    return x**2

deriv = derivative(f, 1.0)
print(deriv)
```

---

# 3. Resolución de Ecuaciones Diferenciales

SciPy proporciona herramientas para resolver ecuaciones diferenciales ordinarias:

- **scipy.odeint()**: Esta función resuelve ecuaciones diferenciales ordinarias.

---

```python
from scipy.integrate import odeint

def model(y, t):
    k = -0.3
    dydt = k * y
    return dydt

y0 = 5
t = np.linspace(0, 20)
result = odeint(model, y0, t)
```

---

# 4. Cálculo del Gradiente

El gradiente es un vector que apunta en la dirección de la máxima tasa de incremento de una función.

- **scipy.gradient()**: Calcula el gradiente de una función.

---

```python
import numpy as np
from scipy import gradient

f = np.array([1, 2, 4, 7, 11, 16], dtype=float)
g = gradient(f)
print(g)
```

---

# 5. Integración Numérica

SciPy ofrece varias funciones para realizar integración numérica:

- **scipy.integrate.quad()**: Para integración numérica de una función de una variable.

---

```python
from scipy.integrate import quad

result, error = quad(lambda x: x**2, 0, 1)
print(result)
```

---

# 6. Encontrar Raíces de Funciones

Para encontrar dónde una función se cruza con el eje x (sus raíces):

- **scipy.fsolve()**: Encuentra las raíces de una función.

---

```python
from scipy.optimize import fsolve

def f(x):
    return x**2 - 4

root = fsolve(f, 1)  # Aproximación inicial de 1
print(root)
```

--- 

# Conclusión

SciPy es una herramienta poderosa para cálculos matemáticos. Con su amplia gama de funciones, puedes resolver una variedad de problemas matemáticos y científicos.

---
Este tutorial proporciona una introducción básica a algunas de las funciones más comunes de SciPy. Puedes expandirlo aún más según las necesidades específicas de tu presentación. ¡Espero que te sea útil!