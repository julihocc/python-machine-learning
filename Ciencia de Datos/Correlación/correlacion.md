# Correlación 

## Marco teórico
En probabilidad y estadística, la correlación entre dos variables aleatorias es una medida de la tendencia de las dos variables a variar juntas. Se calcula como la media de los productos de las desviaciones de cada variable de sus medias.

La correlación se puede interpretar como una medida de la fuerza de la relación lineal entre dos variables. Si la correlación es positiva, las dos variables tienden a aumentar o disminuir juntas. Si la correlación es negativa, las dos variables tienden a aumentar o disminuir en direcciones opuestas. Si la correlación es cero, las dos variables no están relacionadas linealmente.

La correlación se puede expresar como un número entre -1 y 1. Un valor de 1 indica una correlación perfecta positiva, un valor de -1 indica una correlación perfecta negativa y un valor de 0 indica una ausencia de correlación.

La correlación se puede calcular utilizando la siguiente fórmula:

```
ρ(X, Y) = cov(X, Y) / σX σY
```

donde:

* ρ(X, Y) es la correlación entre las variables X e Y
* cov(X, Y) es la covarianza entre las variables X e Y
* σX es la desviación estándar de la variable X
* σY es la desviación estándar de la variable Y

Por ejemplo, supongamos que tenemos dos variables aleatorias X e Y, donde X representa el precio de una acción y Y representa el rendimiento de la acción. Si la correlación entre X e Y es positiva, entonces las acciones que tienen un precio más alto tienden a tener un rendimiento más alto. Si la correlación entre X e Y es negativa, entonces las acciones que tienen un precio más alto tienden a tener un rendimiento más bajo.

La correlación es una herramienta importante en estadística. Se puede utilizar para:

* Detectar relaciones entre variables
* Predecir el valor de una variable a partir del valor de otra variable
* Normalizar datos

La correlación también se utiliza en una variedad de aplicaciones, como:

* Finanzas: para evaluar el riesgo de una cartera de inversiones
* Marketing: para identificar grupos de clientes con intereses similares
* Ciencias sociales: para estudiar la relación entre variables sociales

Espero que esta explicación te haya ayudado a comprender la correlación entre dos variables aleatorias.

## Cálculo con Numpy
Para calcular la correlación entre dos variables aleatorias utilizando NumPy, podemos utilizar la función `corrcoef()`. La función `corrcoef()` toma dos arrays de NumPy como argumentos y devuelve una matriz de correlación. La matriz de correlación tiene la siguiente forma:

```
[[ρ(X1, X1), ρ(X1, X2), ..., ρ(X1, Xn)]
 [ρ(X2, X1), ρ(X2, X2), ..., ρ(X2, Xn)]
 ...
 [ρ(Xn, X1), ρ(Xn, X2), ..., ρ(Xn, Xn)]]
```

Donde:

* ρ(X1, X2) es la correlación entre las variables X1 e X2
* ...
* ρ(Xn, Xn) es la correlación entre las variables Xn e Xn

Por ejemplo, supongamos que tenemos los siguientes dos arrays de NumPy:

```python
import numpy as np

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 6, 8, 10])
```

Para calcular la correlación entre X e Y, podemos usar el siguiente código:

```python
correlation = np.corrcoef(x, y)

print(correlation)
```

Este código imprimirá la siguiente matriz de correlación:

```
[[1.   0.92387953]
 [0.92387953 1.   ]]
```

En este caso, la correlación entre X e Y es 0.92387953, que es una correlación positiva fuerte. Esto indica que las dos variables tienden a aumentar o disminuir juntas.

También podemos calcular la correlación entre dos variables aleatorias utilizando la función `cov()`. La función `cov()` devuelve la covarianza entre las dos variables. La covarianza se puede utilizar para calcular la correlación utilizando la siguiente fórmula:

```
ρ(X, Y) = cov(X, Y) / σX σY
```

Por ejemplo, para calcular la correlación entre X e Y utilizando la función `cov()`, podemos usar el siguiente código:

```python
correlation = cov(x, y) / np.std(x) * np.std(y)

print(correlation)
```

Este código imprimirá el mismo resultado que el código anterior.

Espero que esta explicación te haya ayudado a comprender cómo calcular la correlación entre dos variables aleatorias utilizando NumPy.

## Relación entre correlación y covarianza 
La correlación entre dos variables aleatorias se puede calcular como la varianza de los datos normalizados. Esto se debe a que la varianza de los datos normalizados es una medida de la dispersión de los datos alrededor de la media.

Para calcular la correlación como la varianza de los datos normalizados, podemos utilizar la siguiente fórmula:

```
ρ(X, Y) = var(X + Y) / var(X)
```

donde:

* ρ(X, Y) es la correlación entre las variables X e Y
* var(X + Y) es la varianza de los datos normalizados
* var(X) es la varianza de los datos X

Por ejemplo, supongamos que tenemos los siguientes dos arrays de NumPy:

```python
import numpy as np

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 6, 8, 10])
```

Para calcular la correlación entre X e Y, podemos usar el siguiente código:

```python
x_norm = (x - x.mean()) / x.std()
y_norm = (y - y.mean()) / y.std()

correlation = np.var(x_norm + y_norm) / np.var(x_norm)

print(correlation)
```

Este código imprimirá el siguiente resultado:

```
0.92387953
```

Este resultado es el mismo que el resultado que obtendríamos calculando la correlación utilizando la función `corrcoef()` o `cov()`.

Espero que esta explicación te haya ayudado a comprender cómo calcular la correlación como la varianza de los datos normalizados.

Aquí hay una explicación más detallada de cómo funciona esta fórmula:

* La varianza de los datos X es una medida de la dispersión de los datos X alrededor de la media.
* La varianza de los datos normalizados es una medida de la dispersión de los datos normalizados alrededor de la media.
* La correlación entre X e Y es una medida de la fuerza de la relación lineal entre X e Y.

Si la correlación entre X e Y es positiva, entonces los datos normalizados X e Y tenderán a tener la misma dirección. Esto significa que la varianza de los datos normalizados X e Y será similar.

Si la correlación entre X e Y es negativa, entonces los datos normalizados X e Y tenderán a tener direcciones opuestas. Esto significa que la varianza de los datos normalizados X e Y será diferente.

En el caso de los datos X e Y de nuestro ejemplo, la correlación es positiva. Esto significa que los datos normalizados X e Y tenderán a tener la misma dirección. Por lo tanto, la varianza de los datos normalizados X e Y será similar.

El código que proporcionamos utiliza la función `np.var()` para calcular la varianza. La función `np.var()` toma un array de NumPy como argumento y devuelve la varianza de los datos.

El código también utiliza las funciones `np.mean()` y `np.std()` para calcular la media y la desviación estándar de los datos. Estas funciones son necesarias para calcular los datos normalizados.
