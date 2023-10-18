# Computación Simbólica con SymPy

## **Cálculo Diferencial**

1. **Interpretación Geométrica**: Desde un punto de vista geométrico, la derivada de una función en un punto específico representa la pendiente de la tangente a la curva de la función en ese punto. Es decir, nos dice qué tan inclinada está la tangente en relación con el eje x.

2. **Interpretación Cinemática**: En física, cuando se estudia el movimiento, la derivada de la función de posición con respecto al tiempo nos da la velocidad del objeto. Si derivamos la función de velocidad, obtenemos la aceleración. 

3. **Definición Límite**: Matemáticamente, la derivada de una función  `f`  en un punto `x = a` se define como:

`f'(a) = lim_(h->0) ((f(a+h) - f(a))/h)`

siempre que este límite exista. Esta definición se basa en el cociente incremental de la función.

1. **Notación**: Hay varias formas de denotar la derivada de una función. Las más comunes son:
   - `f'(x)` (Notación de Lagrange)
   - `df/dx` (Notación de Leibniz)
   - `Df` (Notación de Euler)

2. **Aplicaciones**: Las derivadas tienen numerosas aplicaciones en ciencias e ingeniería. Se utilizan para describir tasas de cambio, optimizar funciones, analizar movimientos, entre otras cosas.

3. **Propiedades**: Las derivadas tienen varias propiedades que facilitan su cálculo, como la derivada de una constante (que es cero), la derivada de $x$ (que es 1), reglas de suma, producto, cociente, y la regla de la cadena, entre otras.

En resumen, la derivada de una función nos proporciona información sobre cómo cambia la función. Es una herramienta esencial en cálculo y tiene aplicaciones en una amplia variedad de campos.


### Caso de estudio

**1. Introducción a SymPy**

SymPy es una biblioteca de Python para matemáticas simbólicas. Permite realizar operaciones matemáticas de forma exacta, en lugar de aproximada como lo hacen otras bibliotecas como NumPy.

**2. Conceptos básicos**

- **Símbolos**: En SymPy, las variables deben ser definidas como símbolos.

```python
from sympy import symbols

x, y, z = symbols('x y z')
```

- **Expresiones**: Una vez definidos los símbolos, podemos crear expresiones matemáticas.

```python
expr = x**2 + 2*x + 1
```

**3. Derivación**

Para derivar una función en SymPy, utilizamos la función `diff`.

- **Derivada simple**:

```python
from sympy import diff

expr = x**2 + 2*x + 1
derivada = diff(expr, x)
print(derivada)  # 2*x + 2
```

- **Derivadas de orden superior**:

```python
segunda_derivada = diff(expr, x, 2)
print(segunda_derivada)  # 2
```

- **Derivadas parciales**:

Si tienes una función de varias variables, puedes derivarla respecto a una de ellas manteniendo las otras constantes.

```python
f = x**2 + y**2
df_dx = diff(f, x)  # 2*x
df_dy = diff(f, y)  # 2*y
```

**4. Evaluar derivadas**

Para evaluar una derivada en un punto específico, utilizamos el método `subs`.

```python
derivada = 2*x + 2
valor_en_3 = derivada.subs(x, 3)
print(valor_en_3)  # 8
```

**5. Simplificación**

SymPy puede simplificar expresiones para nosotros usando la función `simplify`.

```python
from sympy import simplify

expr = (x**3 + x**2 - x - 1)/(x**2 + 2*x + 1)
simplified_expr = simplify(expr)
print(simplified_expr)  # x - 1
```

---

## **Solución de Ecuaciones**

Las ecuaciones son expresiones matemáticas que establecen la igualdad entre dos cantidades. Existen diferentes tipos de ecuaciones, y cada tipo tiene sus propios métodos de resolución. A continuación, te presento una descripción general de los tipos más comunes de ecuaciones y los métodos asociados para resolverlas:

1. **Ecuaciones Lineales**: Son ecuaciones de primer grado con una incógnita.
   - Ejemplo: `ax + b = 0`
   - Método de resolución: Despejar la incógnita.

2. **Ecuaciones Cuadráticas**: Son ecuaciones de segundo grado con una incógnita.
   - Ejemplo: `ax^2 + bx + c = 0`
   - Métodos de resolución: 
     - Factorización
     - Fórmula general o cuadrática
     - Completando el trinomio cuadrado perfecto

3. **Ecuaciones Polinómicas**: Son ecuaciones de grado mayor a dos.
   - Ejemplo: `ax^3 + bx^2 + cx + d = 0`
   - Métodos de resolución: 
     - Factorización
     - Teorema de Ruffini
     - Teorema fundamental del álgebra (para encontrar raíces complejas)

4. **Ecuaciones Racionales**: Son ecuaciones que involucran fracciones algebraicas.
   - Método de resolución: Encontrar un denominador común y eliminar los denominadores.

5. **Ecuaciones Radicales**: Son ecuaciones que contienen raíces.
   - Método de resolución: Elevar al cuadrado o al exponente correspondiente para eliminar la raíz y luego resolver la ecuación resultante.

6. **Ecuaciones Exponenciales**: Son ecuaciones donde la incógnita aparece en el exponente.
   - Ejemplo: `a^x = b`
   - Método de resolución: Logaritmos.

7. **Ecuaciones Logarítmicas**: Son ecuaciones que involucran logaritmos.
   - Ejemplo: `log_a(x) = b`
   - Método de resolución: Convertir a forma exponencial y resolver.

8. **Ecuaciones Trigonométricas**: Son ecuaciones que involucran funciones trigonométricas.
   - Ejemplo: `sin(x) = sqrt(3)/2`
   - Método de resolución: Usar identidades trigonométricas y propiedades de las funciones trigonométricas.

9. **Ecuaciones Diferenciales**: Son ecuaciones que involucran derivadas.
   - Métodos de resolución: 
     - Separación de variables
     - Método de coeficientes indeterminados
     - Transformada de Laplace
     - Series de potencias

10. **Ecuaciones en Diferencias**: Son ecuaciones que describen secuencias o series.
       - Método de resolución: Iteración, fórmulas cerradas o transformadas Z.

Estos son solo algunos de los tipos más comunes de ecuaciones y sus métodos de resolución. Es importante mencionar que, dependiendo de la ecuación específica y de las condiciones dadas, puede ser necesario emplear diferentes técnicas o combinaciones de métodos para llegar a la solución.

### Caso de estudio 

**1. Introducción**

SymPy no solo es útil para cálculo diferencial e integral, sino que también es una herramienta poderosa para resolver ecuaciones algebraicas y trascendentales.

**2. Conceptos básicos**

- **Ecuaciones**: En SymPy, una ecuación se crea utilizando la clase `Eq`.

```python
from sympy import Eq, symbols

x = symbols('x')
ecuacion = Eq(x**2 - 5*x + 6, 0)
```

**3. Resolviendo ecuaciones**

Para resolver ecuaciones, utilizamos la función `solve`.

- **Ecuaciones algebraicas**:

```python
from sympy import solve

solucion = solve(ecuacion, x)
print(solucion)  # [2, 3]
```

Esto indica que la ecuación \(x^2 - 5x + 6 = 0\) tiene soluciones \(x = 2\) y \(x = 3\).

- **Ecuaciones trascendentales**:

Supongamos que queremos resolver la ecuación \(\sin(x) = \frac{1}{2}\):

```python
from sympy import sin

ecuacion_trascendental = Eq(sin(x), 1/2)
solucion_trascendental = solve(ecuacion_trascendental, x)
print(solucion_trascendental)
```

**4. Sistemas de ecuaciones**

SymPy también puede resolver sistemas de ecuaciones lineales. Supongamos que queremos resolver el siguiente sistema:

\[ \begin{align*}
x + y &= 5 \\
x - y &= 1 \\
\end{align*} \]

```python
y = symbols('y')
sistema = [
    Eq(x + y, 5),
    Eq(x - y, 1)
]

solucion_sistema = solve(sistema, (x, y))
print(solucion_sistema)  # {x: 3, y: 2}
```

**5. Ecuaciones no lineales**

SymPy también puede intentar resolver ecuaciones no lineales, aunque no siempre garantiza una solución en función de la complejidad de la ecuación.

```python
ecuacion_no_lineal = Eq(x**2 + sin(x), 0)
solucion_no_lineal = solve(ecuacion_no_lineal, x)
print(solucion_no_lineal)
```

---

Estas son algunas de las capacidades de SymPy en cuanto a la resolución de ecuaciones. Es importante recordar que, aunque SymPy es una herramienta poderosa, no todas las ecuaciones tienen soluciones cerradas o pueden ser resueltas simbólicamente. En esos casos, se pueden usar métodos numéricos o aproximaciones.

---

## **Puntos Críticos**

Los puntos críticos de una función son aquellos puntos en los cuales la derivada de la función es cero o no está definida. Estos puntos son esenciales en el análisis matemático, especialmente en el estudio de las funciones y sus gráficas, por las siguientes razones:

1. **Máximos y Mínimos Locales**: Los puntos críticos son candidatos a ser máximos o mínimos locales (también conocidos como relativos) de una función. Un máximo local es un punto donde la función alcanza un valor mayor que en los puntos cercanos, mientras que un mínimo local es un punto donde la función alcanza un valor menor que en los puntos cercanos.

2. **Puntos de Inflexión**: Aunque no todos los puntos críticos son puntos de inflexión, estos últimos suelen estar asociados con cambios en la concavidad de la función. Un punto de inflexión es un punto donde la función cambia de ser cóncava hacia arriba a cóncava hacia abajo, o viceversa.

3. **Análisis de la Gráfica**: Los puntos críticos ayudan a esbozar la gráfica de una función. Al identificar estos puntos y determinar su naturaleza (máximo, mínimo o punto de inflexión), podemos obtener una idea más clara de la forma general de la gráfica de la función.

4. **Optimización**: En problemas de optimización, buscamos valores máximos o mínimos de una función. Los puntos críticos son esenciales en este proceso, ya que nos indican dónde la función podría tener un valor óptimo.

5. **Aplicaciones en Ciencias e Ingeniería**: En muchos contextos prácticos, es necesario encontrar valores óptimos. Por ejemplo, en economía, se pueden buscar niveles de producción que maximicen las ganancias o minimicen los costos. En física, se pueden buscar puntos donde la energía es mínima o máxima. En todos estos casos, el estudio de los puntos críticos es fundamental.

Para determinar la naturaleza de un punto crítico (es decir, si es un máximo, mínimo o punto de inflexión), se pueden usar herramientas como el **test de la segunda derivada**. Si `f''(x) > 0`, el punto es un mínimo local; si `f''(x) < 0`, es un máximo local; y si `f''(x) = 0`, el test es inconcluso y se deben usar otros métodos para determinar la naturaleza del punto.

En resumen, los puntos críticos son esenciales en el análisis matemático porque nos proporcionan información valiosa sobre el comportamiento y las propiedades de una función, y son herramientas clave en la resolución de problemas prácticos en diversas áreas.

### Caso de estudio

**1. Definición de Punto Crítico**

Un punto crítico de una función `f(x)` ocurre donde su derivada es cero (`f'(x) = 0`) o está indefinida.

**2. Conceptos básicos**

- **Símbolos**: En SymPy, las variables deben ser definidas como símbolos.

```python
from sympy import symbols

x = symbols('x')
```

- **Expresiones**: Una vez definidos los símbolos, podemos crear expresiones matemáticas.

```python
f = x**3 - 3*x**2 + 2*x
```

**3. Encontrando la primera derivada**

Para encontrar los puntos críticos, primero derivamos la función.

```python
from sympy import diff

f_prime = diff(f, x)
```

**4. Resolviendo para \( f'(x) = 0 \)**

Usamos la función `solve` para encontrar los valores de \( x \) donde \( f'(x) = 0 \).

```python
from sympy import solve

critical_points = solve(f_prime, x)
```

**5. Determinando la naturaleza de los puntos críticos**

Para determinar si un punto crítico es un máximo, mínimo o punto de inflexión, podemos usar la segunda derivada, `f''(x)`.

- Si `f''(x) > 0`, el punto es un mínimo local.
- Si `f''(x) < 0`, el punto es un máximo local.
- Si `f''(x) = 0`, el test es inconclusivo.

```python
f_double_prime = diff(f_prime, x)

for point in critical_points:
    if f_double_prime.subs(x, point) > 0:
        print(f"{point} es un mínimo local.")
    elif f_double_prime.subs(x, point) < 0:
        print(f"{point} es un máximo local.")
    else:
        print(f"{point} es no es concluyente.")
```


Estos pasos te permitirán encontrar y clasificar los puntos críticos de una función utilizando SymPy. Es importante recordar que los puntos críticos son lugares donde la función puede cambiar de dirección, pero no garantizan que la función tenga un máximo o mínimo absoluto. Para determinar máximos o mínimos absolutos, es posible que también debas evaluar los valores de la función en los extremos de su dominio o en cualquier punto donde la función esté indefinida.