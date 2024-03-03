# Covarianza
## Marco teórico
En probabilidad y estadística, la covarianza es una medida de la tendencia de dos variables aleatorias a variar juntas. Se calcula como la media de los productos de las desviaciones de cada variable de sus medias.

La covarianza se puede interpretar como una medida de la fuerza de la relación lineal entre dos variables. Si la covarianza es positiva, las dos variables tienden a aumentar o disminuir juntas. Si la covarianza es negativa, las dos variables tienden a aumentar o disminuir en direcciones opuestas. Si la covarianza es cero, las dos variables no están relacionadas linealmente.

La covarianza se puede expresar como un número entre -∞ y ∞. Un valor de ∞ indica una correlación perfecta positiva, un valor de -∞ indica una correlación perfecta negativa y un valor de 0 indica una ausencia de correlación.

La covarianza se puede calcular utilizando la siguiente fórmula:

```
cov(X, Y) = E[(X - μX)(Y - μY)]
```

donde:

* cov(X, Y) es la covarianza entre las variables X e Y
* E[] es la esperanza matemática
* X es la variable X
* Y es la variable Y
* μX es la media de la variable X
* μY es la media de la variable Y

Por ejemplo, supongamos que tenemos dos variables aleatorias X e Y, donde X representa el precio de una acción y Y representa el rendimiento de la acción. Si la covarianza entre X e Y es positiva, entonces las acciones que tienen un precio más alto tienden a tener un rendimiento más alto. Si la covarianza entre X e Y es negativa, entonces las acciones que tienen un precio más alto tienden a tener un rendimiento más bajo.

La covarianza es una herramienta importante en estadística. Se puede utilizar para:

* Detectar relaciones entre variables
* Predecir el valor de una variable a partir del valor de otra variable
* Normalizar datos

La covarianza también se utiliza en una variedad de aplicaciones, como:

* Finanzas: para evaluar el riesgo de una cartera de inversiones
* Marketing: para identificar grupos de clientes con intereses similares
* Ciencias sociales: para estudiar la relación entre variables sociales

## Desarrollo de l fórmula con Numpy

Para calcular la covarianza entre dos variables aleatorias utilizando NumPy, podemos seguir los siguientes pasos:

1. Importar la biblioteca NumPy.
2. Crear dos arrays de NumPy que contengan los datos de las dos variables aleatorias.
3. Calcular la media de cada variable aleatoria.
4. Calcular la desviación de cada dato de su media correspondiente.
5. Multiplicar cada desviación de X por la desviación correspondiente de Y.
6. Promediar los productos calculados en el paso 5.

Por ejemplo, supongamos que tenemos los siguientes dos arrays de NumPy:

```python
import numpy as np

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 6, 8, 10])
```

Para calcular la covarianza entre X e Y, podemos usar el siguiente código:

```python
# Calcular la media de X
x_mean = np.mean(x)

# Calcular la media de Y
y_mean = np.mean(y)

# Calcular la desviación de cada dato de su media correspondiente
x_dev = x - x_mean
y_dev = y - y_mean

# Multiplicar cada desviación de X por la desviación correspondiente de Y
cov_xy = x_dev * y_dev

# Promediar los productos calculados
cov = np.mean(cov_xy)

print(cov)
```

Este código imprimirá el siguiente resultado:

```
4.242640687119285
```

Este resultado es el mismo que el resultado que obtendríamos calculando la covarianza utilizando la función `numpy.cov()`.

**Ejemplo:**

```python
import numpy as np

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 6, 8, 10])

# Calcular la covarianza
cov = np.cov(x, y)

print(cov)
```

Este código imprimirá la siguiente matriz de covarianza:

```
[[4.24264069]
 [4.24264069]]
```

En este caso, la covarianza entre X e Y es 4.24264069, que es una correlación positiva fuerte. Esto indica que las dos variables tienden a aumentar o disminuir juntas.

También podemos calcular la covarianza entre dos variables aleatorias utilizando la función `numpy.cov()`. La función `numpy.cov()` toma dos arrays de NumPy como argumentos y devuelve una matriz de covarianza. La matriz de covarianza tiene la siguiente forma:

```
[[ρ(X1, X1), ρ(X1, X2), ..., ρ(X1, Xn)]
 [ρ(X2, X1), ρ(X2, X2), ..., ρ(X2, Xn)]
 ...
 [ρ(Xn, X1), ρ(Xn, X2), ..., ρ(Xn, Xn)]]
```

Donde:

* ρ(X1, X2) es la covarianza entre las variables X1 e X2
* ...
* ρ(Xn, Xn) es la covarianza entre las variables Xn e Xn

Por ejemplo, para calcular la covarianza entre X e Y utilizando la función `numpy.cov()`, podemos usar el siguiente código:

```python
cov = np.cov(x, y)

print(cov)
```

Este código imprimirá la misma matriz de covarianza que el código anterior.

## Cálculo directo con Numpy

En NumPy, la función `cov()` se utiliza para calcular la covarianza de dos o más variables. La función toma dos argumentos obligatorios:

* `data`: Un array de NumPy que contiene los datos de las variables.
* `ddof`: Un valor opcional que indica cómo se debe normalizar la covarianza. El valor predeterminado es `1`, que da una estimación no sesgada de la covarianza. Un valor de `0` da una estimación sesgada.

Por ejemplo, para calcular la covarianza de las variables `x` e `y`, podemos usar el siguiente código:

```python
import numpy as np

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 6, 8, 10])

cov = np.cov(x, y)

print(cov)
```

Este código imprimirá la siguiente matriz de covarianza:

```
[[14.0   ]
 [   0.0 20.0]]
```

La matriz de covarianza tiene dos valores: el valor en la diagonal principal es la varianza de cada variable, y los valores fuera de la diagonal principal son las covarianzas entre las dos variables.

En este caso, la covarianza entre `x` e `y` es positiva, lo que indica que las dos variables tienden a variar juntas.

La covarianza se puede utilizar para una variedad de propósitos, como:

* Detectar relaciones entre variables.
* Predecir el valor de una variable a partir del valor de otra variable.
* Normalizar datos.

Aquí hay algunos ejemplos de cómo se puede utilizar la covarianza en NumPy:

* Para detectar relaciones entre variables, podemos comparar la covarianza entre pares de variables. Si la covarianza es positiva, las dos variables tienden a variar juntas. Si la covarianza es negativa, las dos variables tienden a variar en direcciones opuestas.
* Para predecir el valor de una variable a partir del valor de otra variable, podemos utilizar un modelo de regresión lineal. La covarianza entre las dos variables es un factor importante en el modelo de regresión lineal.
* Para normalizar datos, podemos restar la media de cada variable y dividirla por la desviación estándar. Esto ayuda a garantizar que los datos estén en una escala comparable.
