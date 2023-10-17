# Gráficas y visualización

**Introducción a la visualización de datos con Matplotlib**

La visualización de datos es el proceso de representar datos de forma visual para facilitar su comprensión. Es una herramienta esencial para el análisis de datos, ya que permite identificar patrones y tendencias que pueden pasar desapercibidos en un conjunto de datos crudo.

Matplotlib es una biblioteca de Python para la generación de gráficos y visualizaciones de datos. Es una herramienta potente y flexible que puede utilizarse para crear una amplia gama de gráficos, desde simples gráficos de líneas hasta diagramas complejos.

**¿Cómo funciona Matplotlib?**

Matplotlib funciona creando un objeto `Figure` que representa el lienzo en el que se dibujarán los gráficos. A continuación, se crean objetos `Axes` para representar los ejes de los gráficos. Finalmente, se utilizan métodos de los objetos `Axes` para dibujar los datos.

**¿Cómo crear un gráfico simple con Matplotlib?**

Para crear un gráfico simple con Matplotlib, podemos utilizar la función `plot()`. Esta función toma dos argumentos: un vector de datos para el eje x y un vector de datos para el eje y.

Por ejemplo, para crear un gráfico de líneas que represente la temperatura media diaria en un mes, podríamos utilizar el siguiente código:



```Python
import matplotlib.pyplot as plt

# Datos
x = [1, 2, 3, 4, 5]
y = [10, 12, 14, 16, 18]

# Gráfico
plt.plot(x, y)

# Mostrar el gráfico
plt.show()
```

Este código creará el siguiente gráfico:

```
    10
    12
    14
    16
    18
    
```

**Personalización de gráficos con Matplotlib**

Matplotlib ofrece una amplia gama de opciones para personalizar los gráficos. Por ejemplo, podemos cambiar el color, el estilo y el tamaño de las líneas, o añadir etiquetas a los ejes.

Para personalizar un gráfico, podemos utilizar los métodos de los objetos `Axes`. Por ejemplo, para cambiar el color de las líneas en el gráfico anterior, podríamos utilizar el siguiente código:



```Python
# Cambiar el color de las líneas
plt.plot(x, y, color='red')
```

Este código creará el siguiente gráfico:

```
    10
    12
    14
    16
    18
    
```

##  **Tipos de gráficos con Matplotlib**

Matplotlib ofrece una amplia gama de tipos de gráficos, incluyendo:

-   Gráficos de líneas
-   Gráficos de barras
-   Gráficos de dispersión
-   Gráficos de sectores
-   Diagramas de cajas
-   Histogramas

**Gráficos de líneas**

Los gráficos de líneas son un tipo de gráfico que se utiliza para mostrar la evolución de una variable a lo largo del tiempo. Se representan mediante una serie de puntos conectados por líneas.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt

# Datos
x = [1, 2, 3, 4, 5]
y = [10, 12, 14, 16, 18]

# Gráfico
plt.plot(x, y)

# Mostrar el gráfico
plt.show()
```

Este código creará el siguiente gráfico:

```
    10
    12
    14
    16
    18
    
```

**Gráficos de barras**

Los gráficos de barras son un tipo de gráfico que se utiliza para comparar dos o más variables. Se representan mediante una serie de barras verticales u horizontales.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt

# Datos
x = ['A', 'B', 'C']
y = [10, 20, 30]

# Gráfico
plt.bar(x, y)

# Mostrar el gráfico
plt.show()
```

Este código creará el siguiente gráfico:

```
    A
    10
    B
    20
    C
    30
    
```

**Gráficos de dispersión**

Los gráficos de dispersión son un tipo de gráfico que se utiliza para mostrar la relación entre dos variables. Se representan mediante una serie de puntos que se conectan mediante líneas.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt

# Datos
x = [1, 2, 3, 4, 5]
y = [10, 12, 14, 16, 18]

# Gráfico
plt.scatter(x, y)

# Mostrar el gráfico
plt.show()
```

Este código creará el siguiente gráfico:

```
    10
    12
    14
    16
    18
    
```

**Gráficos de sectores**

Los gráficos de sectores son un tipo de gráfico que se utiliza para mostrar la distribución de una variable. Se representan mediante una serie de sectores circulares.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt

# Datos
labels = ['A', 'B', 'C']
values = [10, 20, 30]

# Gráfico
plt.pie(values, labels=labels)

# Mostrar el gráfico
plt.show()
```

Este código creará el siguiente gráfico:

```
    A
    B
    C
    
```

**Diagramas de cajas**

Los diagramas de cajas son un tipo de gráfico que se utiliza para mostrar la distribución de una variable. Se representan mediante una caja, bigotes y puntos.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt

# Datos
data = [1, 2, 3, 4, 5]

# Gráfico
plt.boxplot(data)

# Mostrar el gráfico
plt.show()
```

Este código creará el siguiente gráfico:

```
    2.5
    2.0
    3.0
    4.0
    5.0
    
```

**Histogramas**

Los histogramas son un tipo de gráfico que se utiliza para mostrar la distribución de una variable. Se representan mediante una serie de barras.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt

# Datos
data = [1, 2, 3, 4, 5]

# Gráfico
plt.hist(data)

# Mostrar el gráfico
plt.show()
```

Este código creará el siguiente gráfico:

```
    1.0
    2.0
    3.0
    4.0
    5.0
    
```

## El objeto `Figure`

El objeto `Figure` en Matplotlib representa el lienzo en el que se dibujarán los gráficos. Es un objeto de alto nivel que proporciona métodos para crear, personalizar y mostrar gráficos.

**Creación de un objeto Figure**

Para crear un objeto `Figure`, podemos utilizar la función `Figure()`. Esta función toma dos argumentos opcionales: el ancho y la altura del lienzo en píxeles.

Python

```
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))
```

Este código creará un objeto `Figure` con un ancho de 10 píxeles y una altura de 5 píxeles.

**Personalización de un objeto Figure**

Podemos personalizar un objeto `Figure` utilizando los métodos y atributos de la clase `Figure`. Por ejemplo, podemos cambiar el título del gráfico, el fondo del lienzo, o la resolución del gráfico.



```Python
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))

# Personalizar el Figure
fig.suptitle('Titulo del gráfico')
fig.patch.set_facecolor('white')
fig.canvas.set_dpi(100)
```

Este código creará un objeto `Figure` con un título, un fondo blanco y una resolución de 100 píxeles por pulgada.

**Mostrar un objeto Figure**

Para mostrar un objeto `Figure`, podemos utilizar la función `show()`. Esta función mostrará el gráfico en la pantalla.



```Python
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))

# Personalizar el Figure
fig.suptitle('Titulo del gráfico')
fig.patch.set_facecolor('white')
fig.canvas.set_dpi(100)

# Mostrar el Figure
plt.show()
```

Este código creará un gráfico con un título, un fondo blanco y una resolución de 100 píxeles por pulgada. El gráfico se mostrará en la pantalla.

El objeto `Figure` es una herramienta esencial para crear gráficos con Matplotlib. Proporciona métodos y atributos para personalizar el aspecto y el comportamiento de los gráficos.

## El objeto `Axes`

El objeto `Axes` en Matplotlib representa un área de dibujo en un objeto `Figure`. Es un objeto de bajo nivel que proporciona métodos para dibujar datos, personalizar el aspecto de los gráficos y añadir elementos al gráfico.

**Creación de un objeto Axes**

Para crear un objeto `Axes`, podemos utilizar la función `add_subplot()`. Esta función toma dos argumentos obligatorios: el número de filas y el número de columnas en las que se colocará el objeto `Axes`. También podemos especificar el índice del objeto `Axes` en la matriz.



```Python
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))

# Crear un objeto Axes
ax = fig.add_subplot(111)
```

Este código creará un objeto `Axes` que ocupará toda la figura.

**Personalización de un objeto Axes**

Podemos personalizar un objeto `Axes` utilizando los métodos y atributos de la clase `Axes`. Por ejemplo, podemos cambiar el título del eje x, el título del eje y, o el rango de los ejes.



```Python
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))

# Crear un objeto Axes
ax = fig.add_subplot(111)

# Personalizar el Axes
ax.set_xlabel('Titulo del eje x')
ax.set_ylabel('Titulo del eje y')
ax.set_xlim([0, 10])
ax.set_ylim([0, 100])
```

Este código creará un objeto `Axes` con un título para el eje x, un título para el eje y, y un rango de [0, 10] para el eje x y [0, 100] para el eje y.

**Dibujar datos en un objeto Axes**

Para dibujar datos en un objeto `Axes`, podemos utilizar los métodos `plot()`, `scatter()`, `bar()`, etc. Estos métodos toman dos argumentos obligatorios: el vector de datos para el eje x y el vector de datos para el eje y.



```Python
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))

# Crear un objeto Axes
ax = fig.add_subplot(111)

# Dibujar datos
ax.plot([1, 2, 3, 4, 5], [10, 12, 14, 16, 18])
```

Este código creará un gráfico de líneas con cinco puntos.

**Añadir elementos a un objeto Axes**

Podemos añadir elementos a un objeto `Axes` utilizando los métodos y atributos de la clase `Axes`. Por ejemplo, podemos añadir una leyenda, una cuadrícula, o un texto.



```Python
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))

# Crear un objeto Axes
ax = fig.add_subplot(111)

# Añadir elementos
ax.plot([1, 2, 3, 4, 5], [10, 12, 14, 16, 18])
ax.legend()
ax.grid()
ax.text(0.5, 0.5, 'Este es un texto')
```

Este código creará un gráfico de líneas con una leyenda, una cuadrícula y un texto.

El objeto `Axes` es una herramienta esencial para crear gráficos con Matplotlib. Proporciona métodos y atributos para dibujar datos, personalizar el aspecto de los gráficos y añadir elementos al gráfico.

### Propiedades del objeto `Axes`

Las propiedades del objeto Axes en Matplotlib son atributos que se utilizan para personalizar el aspecto y el comportamiento de los gráficos. Estas propiedades se pueden establecer utilizando el método `set()` o el atributo directamente.

**Algunas de las propiedades más comunes del objeto Axes incluyen:**

-   **Titulo del eje x:** `xlabel`
-   **Titulo del eje y:** `ylabel`
-   **Rango del eje x:** `xlim`
-   **Rango del eje y:** `ylim`
-   **Título del gráfico:** `title`
-   **Leyenda:** `legend`
-   **Cuadrícula:** `grid`
-   **Color de fondo:** `facecolor`
-   **Color de las líneas:** `linecolor`
-   **Ancho de las líneas:** `linewidth`
-   **Estilo de las líneas:** `linestyle`
-   **Tamaño de la fuente:** `fontsize`

**Ejemplo:**

Python

```
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))

# Crear un objeto Axes
ax = fig.add_subplot(111)

# Personalizar el Axes
ax.set_xlabel('Titulo del eje x', fontsize=16)
ax.set_ylabel('Titulo del eje y', fontsize=16)
ax.set_xlim([0, 10])
ax.set_ylim([0, 100])
ax.set_title('Título del gráfico', fontsize=20)
ax.legend()
ax.grid()
ax.set_facecolor('white')
ax.plot([1, 2, 3, 4, 5], [10, 12, 14, 16, 18], color='red', linewidth=2, linestyle='--')

# Mostrar el gráfico
plt.show()
```

Este código creará un gráfico de líneas con un título, una leyenda, una cuadrícula y un texto. El título del eje x será "Titulo del eje x" y tendrá un tamaño de fuente de 16. El título del eje y será "Titulo del eje y" y tendrá un tamaño de fuente de 16. El rango del eje x será [0, 10] y el rango del eje y será [0, 100]. El color de fondo del gráfico será blanco. Las líneas serán de color rojo, con un ancho de 2 y un estilo de línea discontinuo.

**Para obtener más información sobre las propiedades del objeto Axes, consulte la documentación de Matplotlib.**

## Diseño avanzado de ejes

El diseño avanzado del objeto Axes en Matplotlib permite a los usuarios personalizar aún más el aspecto y el comportamiento de los gráficos. Este diseño avanzado se basa en los siguientes conceptos:

-   **Leyendas:** Las leyendas se utilizan para identificar las diferentes series de datos que se muestran en un gráfico. Las leyendas se pueden personalizar en términos de su ubicación, tamaño y formato.
-   **Cuadrículas:** Las cuadrículas se utilizan para facilitar la lectura de los gráficos. Las cuadrículas se pueden personalizar en términos de su color, ancho y estilo.
-   **Ticks:** Los ticks se utilizan para etiquetar los ejes de los gráficos. Los ticks se pueden personalizar en términos de su ubicación, tamaño y formato.
-   **Ticks labels:** Los ticks labels son las etiquetas que se muestran junto a los ticks. Los ticks labels se pueden personalizar en términos de su contenido, tamaño y formato.
-   **Ticks positions:** Las ticks positions son las posiciones de los ticks en los ejes. Las ticks positions se pueden personalizar en términos de su ubicación y rango.
-   **Axis properties:** Las axis properties son las propiedades de los ejes de los gráficos. Estas propiedades incluyen el ancho, el color y el estilo de los ejes.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt

# Crear un objeto Figure
fig = plt.Figure(figsize=(10, 5))

# Crear un objeto Axes
ax = fig.add_subplot(111)

# Personalizar el Axes
ax.set_xlabel('Titulo del eje x', fontsize=16)
ax.set_ylabel('Titulo del eje y', fontsize=16)
ax.set_xlim([0, 10])
ax.set_ylim([0, 100])
ax.set_title('Título del gráfico', fontsize=20)
ax.legend()
ax.grid()
ax.set_facecolor('white')
ax.plot([1, 2, 3, 4, 5], [10, 12, 14, 16, 18], color='red', linewidth=2, linestyle='--')

# Personalizar los ticks
ax.set_xticks([0, 2, 4, 6, 8, 10])
ax.set_yticks([0, 25, 50, 75, 100])
ax.set_xticklabels(['0', '2', '4', '6', '8', '10'])
ax.set_yticklabels(['0', '25', '50', '75', '100'])

# Personalizar la leyenda
ax.legend(loc='upper left', fontsize=16)

# Mostrar el gráfico
plt.show()
```

Este código creará un gráfico de líneas con un título, una leyenda, una cuadrícula y un texto. Los ticks se personalizarán para que aparezcan en los puntos [0, 2, 4, 6, 8, 10] en el eje x y [0, 25, 50, 75, 100] en el eje y. Los ticks labels se personalizarán para que aparezcan como "0", "2", "4", "6", "8", "10" en el eje x y "0", "25", "50", "75", "100" en el eje y. La leyenda se personalizará para que aparezca en la esquina superior izquierda del gráfico y tenga un tamaño de fuente de 16.

Aquí hay algunos ejemplos adicionales de cómo se puede utilizar el diseño avanzado del objeto Axes:

-   Para personalizar el color y el ancho de los ejes, podemos utilizar los métodos `set_axis_bgcolor()` y `set_axis_linewidth()`.
-   Para personalizar el color y el ancho de las líneas de la cuadrícula, podemos utilizar los métodos `set_grid_color()` y `set_grid_linewidth()`.
-   Para personalizar el formato de los ticks labels, podemos utilizar los métodos `set_xticklabels()` y `set_yticklabels()`.
-   Para personalizar la ubicación de los ticks, podemos utilizar los métodos `set_xticks()` y `set_yticks()`.

Con un poco de práctica, podemos utilizar el diseño avanzado

## Gráfico de mapas de colores

Los gráficos de mapas de colores son un tipo de gráfico que utiliza colores para representar datos. Los datos se mapean a un rango de colores, y cada color representa un valor diferente. Los gráficos de mapas de colores se utilizan a menudo para visualizar datos continuos, como temperaturas, alturas o densidades.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt
import numpy as np

# Datos
x = np.linspace(0, 10, 100)
y = x * x

# Gráfico
plt.plot(x, y, cmap='viridis')

# Mostrar el gráfico
plt.show()
```

Este código creará un gráfico de mapa de colores que representa la función y=x2. El color de cada punto del gráfico representa su valor en la función. Los colores más oscuros representan valores más altos, mientras que los colores más claros representan valores más bajos.

**Tipos de mapas de colores:**

Hay muchos tipos diferentes de mapas de colores disponibles. Algunos de los mapas de colores más comunes incluyen:

-   **Jet:** Este mapa de colores utiliza colores del rojo al azul para representar valores del menor al mayor.
-   **Viridis:** Este mapa de colores utiliza colores del azul al verde para representar valores del menor al mayor.
-   **Inferno:** Este mapa de colores utiliza colores del rojo al negro para representar valores del menor al mayor.
-   **Plasma:** Este mapa de colores utiliza colores del azul al rojo para representar valores del menor al mayor.

**Elección del mapa de colores adecuado:**

La elección del mapa de colores adecuado es importante para que los datos sean visibles y comprensibles. El mapa de colores debe ser elegido de manera que los valores más altos sean fácilmente distinguibles de los valores más bajos.

**Personalización de los gráficos de mapas de colores:**

Los gráficos de mapas de colores se pueden personalizar de varias maneras. Por ejemplo, podemos cambiar el rango de colores, el estilo de los colores o la ubicación de los colores.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt
import numpy as np

# Datos
x = np.linspace(0, 10, 100)
y = x * x

# Gráfico
plt.plot(x, y, cmap='viridis', vmin=0, vmax=100)

# Mostrar el gráfico
plt.show()
```

Este código creará un gráfico de mapa de colores que representa la función y=x2. El rango de colores se ha cambiado para que los valores más altos sean más fáciles de distinguir.

**Conclusiones:**

Los gráficos de mapas de colores son una herramienta poderosa para visualizar datos continuos. Con una elección adecuada del mapa de colores, podemos crear gráficos que sean claros y comprensibles.

## Gráficos tridimensionales

Para trazar gráficos tridimensionales en Matplotlib, podemos utilizar la clase `Axes3D`. Esta clase representa un área de dibujo en tres dimensiones.

**Creación de un objeto Axes3D:**

Para crear un objeto `Axes3D`, podemos utilizar la función `add_subplot3d()`. Esta función toma dos argumentos obligatorios: el número de filas y el número de columnas en las que se colocará el objeto `Axes3D`. También podemos especificar el índice del objeto `Axes3D` en la matriz.



```Python
import matplotlib.pyplot as plt
import numpy as np

# Crear un objeto Figure
fig = plt.figure(figsize=(10, 5))

# Crear un objeto Axes3D
ax = fig.add_subplot(111, projection='3d')
```

Este código creará un objeto `Axes3D` que ocupará toda la figura.

**Trazando datos en 3D:**

Para trazar datos en 3D, podemos utilizar los métodos `plot()`, `scatter()`, `surface()`, etc. Estos métodos toman tres argumentos obligatorios: los valores del eje x, los valores del eje y y los valores del eje z.



```Python
import matplotlib.pyplot as plt
import numpy as np

# Crear un objeto Figure
fig = plt.figure(figsize=(10, 5))

# Crear un objeto Axes3D
ax = fig.add_subplot(111, projection='3d')

# Datos
x = np.linspace(0, 10, 100)
y = np.linspace(0, 10, 100)
z = x * y

# Gráfico
ax.plot(x, y, z)

# Mostrar el gráfico
plt.show()
```

Este código creará un gráfico de líneas en 3D que representa la función z=x∗y.

**Personalización de los gráficos tridimensionales:**

Los gráficos tridimensionales se pueden personalizar de varias maneras. Por ejemplo, podemos cambiar el color de las líneas, el estilo de las líneas o la ubicación de los ejes.

**Ejemplo:**



```Python
import matplotlib.pyplot as plt
import numpy as np

# Crear un objeto Figure
fig = plt.figure(figsize=(10, 5))

# Crear un objeto Axes3D
ax = fig.add_subplot(111, projection='3d')

# Datos
x = np.linspace(0, 10, 100)
y = np.linspace(0, 10, 100)
z = x * y

# Gráfico
ax.plot(x, y, z, color='red', linestyle='--')

# Personalización
ax.set_xlabel('Eje x')
ax.set_ylabel('Eje y')
ax.set_zlabel('Eje z')

# Mostrar el gráfico
plt.show()
```

Este código creará un gráfico de líneas en 3D que representa la función z=x∗y. Las líneas serán de color rojo y tendrán un estilo de línea discontinuo. Los ejes también se han personalizado con etiquetas.

**Conclusiones:**

Los gráficos tridimensionales son una herramienta poderosa para visualizar datos en tres dimensiones. Con una selección adecuada de datos y parámetros, podemos crear gráficos que sean claros y comprensibles.

**Aquí hay algunos consejos para trazar gráficos tridimensionales:**

-   Utilice colores y etiquetas claros para que los datos sean fáciles de visualizar.
-   Use un escalado adecuado para que los datos se vean nítidos y bien definidos.
-   Evite superponer demasiados datos, ya que esto puede dificultar la visualización.
-   Utilice métodos de visualización adecuados para los tipos de datos que está trazando.

Con un poco de práctica, podemos crear gráficos tridimensionales que son claros, concisos y efectivos.

## Resumen 

En este tutorial, hemos visto los siguientes temas relacionados con la creación de gráficos con Matplotlib:

-   **Objetos Figure y Axes:** Los objetos Figure y Axes son los bloques de construcción básicos de los gráficos de Matplotlib. El objeto Figure representa el lienzo en el que se dibujarán los gráficos, mientras que el objeto Axes representa un área de dibujo en el que se pueden dibujar datos.
-   **Métodos para dibujar datos:** Matplotlib proporciona una variedad de métodos para dibujar datos, como `plot()`, `scatter()`, `bar()`, etc. Estos métodos toman dos argumentos obligatorios: los valores del eje x y los valores del eje y.
-   **Personalización de los gráficos:** Los gráficos se pueden personalizar de varias maneras, como cambiando el color, el estilo y el tamaño de las líneas, así como la ubicación de los ejes.
-   **Gráficos de mapas de colores:** Los gráficos de mapas de colores son un tipo de gráfico que utiliza colores para representar datos. Los datos se mapean a un rango de colores, y cada color representa un valor diferente.
-   **Gráficos tridimensionales:** Los gráficos tridimensionales se utilizan para visualizar datos en tres dimensiones. Matplotlib proporciona la clase `Axes3D` para crear gráficos tridimensionales.

**Conclusión:**

Matplotlib es una biblioteca de Python poderosa y flexible para la visualización de datos. Con un poco de práctica, podemos crear gráficos que son claros, concisos y efectivos.

**Aquí hay algunos consejos generales para crear gráficos con Matplotlib:**

-   Utilice colores y etiquetas claros para que los datos sean fáciles de visualizar.
-   Use un escalado adecuado para que los datos se vean nítidos y bien definidos.
-   Evite superponer demasiados datos, ya que esto puede dificultar la visualización.
-   Utilice métodos de visualización adecuados para los tipos de datos que está trazando.

Siguiendo estos consejos, podemos crear gráficos que son claros, concisos y efectivos.