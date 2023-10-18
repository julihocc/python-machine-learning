# Correlación

## Concepto

La correlación entre variables es una medida de la relación lineal entre dos variables. Una correlación positiva indica que las variables tienden a aumentar o disminuir juntas. Una correlación negativa indica que las variables tienden a aumentar o disminuir en direcciones opuestas. Una correlación de 0 indica que no hay relación lineal entre las variables.

El coeficiente de correlación de Pearson es una medida de la correlación entre dos variables continuas. Se calcula mediante la siguiente fórmula:

```
r = cov(X, Y) / σ_X σ_Y
```

donde:

* r es el coeficiente de correlación de Pearson
* cov(X, Y) es la covarianza entre las variables X e Y
* σ_X es la desviación estándar de la variable X
* σ_Y es la desviación estándar de la variable Y

La covarianza es una medida de la tendencia de dos variables a variar juntas. Se calcula mediante la siguiente fórmula:

```
cov(X, Y) = ∑(x_i - μ_X)(y_i - μ_Y) / n
```

donde:

* cov(X, Y) es la covarianza entre las variables X e Y
* x_i es el valor de la variable X en la observación i
* μ_X es la media de la variable X
* y_i es el valor de la variable Y en la observación i
* μ_Y es la media de la variable Y
* n es el número de observaciones

Una vez calculado el coeficiente de correlación de Pearson, se puede interpretar de la siguiente manera:

* r > 0,8: correlación fuerte
* 0,6 < r < 0,8: correlación moderada
* 0,4 < r < 0,6: correlación débil
* r < 0,4: no hay correlación

Un mapa de calor es una representación visual de una matriz de datos. En el caso de la correlación entre variables, un mapa de calor muestra el coeficiente de correlación entre cada par de variables.

Para crear un mapa de calor de la correlación entre variables, se pueden seguir los siguientes pasos:

1. Calcular el coeficiente de correlación de Pearson entre cada par de variables.
2. Crear una matriz de datos con los coeficientes de correlación.
3. Utilizar una biblioteca de visualización de datos para crear un mapa de calor a partir de la matriz de datos.

## Aplicaciones

En Python, se puede utilizar la biblioteca matplotlib para crear un mapa de calor de la correlación entre variables. El siguiente código muestra cómo crear un mapa de calor de la correlación entre las variables del conjunto de datos de precios de casas de Kaggle:

```python
import pandas as pd
import matplotlib.pyplot as plt

# Cargar el conjunto de datos
data = pd.read_csv("house_prices.csv")

# Calcular la matriz de correlación
correlation = data.corr()

# Crear el mapa de calor
plt.matshow(correlation)
plt.title("Matriz de correlación")
plt.show()
```

Este código crea un mapa de calor con un color más oscuro que indica una mayor correlación. En el mapa de calor, se puede observar que el número de dormitorios y el precio de venta están correlacionados positivamente. Esto significa que las casas con más dormitorios suelen tener un precio de venta más alto. También se puede observar que el año de construcción y el precio de venta están correlacionados negativamente. Esto significa que las casas más antiguas suelen tener un precio de venta más bajo.

La correlación entre variables es una herramienta útil para comprender la relación entre las variables de un conjunto de datos. Un mapa de calor puede ser una forma eficaz de visualizar la correlación entre variables.