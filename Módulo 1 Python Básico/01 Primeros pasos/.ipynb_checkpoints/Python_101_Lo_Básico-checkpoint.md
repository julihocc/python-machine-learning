# Python con ejemplos
# Lo básico

Bienvenidos al curso de Python con Ejemplos


```python
"""
Para continuar con la gloriosa tradición de un curso introductorio, escribiremos
como nuestro primer programa, el ya famoso `Hola Mundo!`, es decir, instruiremos 
a la computadora a que imprima esta leyenda en la pantalla.
"""
print("Hola mundo!")
```

    Hola mundo!
    


```python
"""
COmo observas, todo el texto que este escrito en este mismo formato es IGNORADO
por la computadora. Esto le llamamos un *comentario*, que es útil para que 
nuestros colaboradores entiendan que estamos tratando de hacer.
"""
# Otra opción para comentar es poner el texto después de un hashtag
# Pero esto sólo fuciona para una línea
# Por lo que si quisieras hacer un comentario muy largo
# Como el que estoy escribiendo, tendrías que usar un hashtag
# Por cada renglón que escribas y la verdad es muy 
# Cansado y tedioso. 
# Ocupa este formato sólo para comentarios cortos!
```




    '\nCOmo observas, todo el texto que este escrito en este mismo formato es IGNORADO\npor la computadora. Esto le llamamos un *comentario*, que es útil para que \nnuestros colaboradores entiendan que estamos tratando de hacer.\n'




```python
"""
Lo primero que debemos saber es como declarar variables, que puede  ser decimales,
cadenas (de caracteres), enteros o booleanos (falso/verdaderas)
En Python es muy fácil! Sólo tienes que darles un nombre y asignarles un valor.

Además, podemos imprimir su valor para verlo en pantalla.
"""
algun_decimal = 3.14159
print(algun_decimal)

alguna_literal = "Hola"
print(alguna_literal)

algun_entero = 2019
print(algun_entero)

algun_booleano = True # El otro valor booleano es False 
print(algun_booleano)

```

    3.14159
    Hola
    2019
    True
    


```python
"""
Podemos realizar operaciones entre variables del mismo tipo. Intentemos primero
con números decimales.
"""
x = 1.5
y = 2.4
print(x+y)
print(x-y)
print(x*y)
print(x/y)
```

    3.9
    -0.8999999999999999
    3.5999999999999996
    0.625
    


```python
"""
¿Qué pasa si intentamos los mismo con número enteros?
"""
x = 3
y = 2
print(x+y)
print(x-y)
print(x*y)
print(x/y)
```

    5
    1
    6
    1.5
    


```python
"""
Como puedes observar, la división entre dos enteros no necesariamente es entera.
Sin embargo, a veces necesitamos calcular el cociente y el residuo de tales
divisiones. Para esto tenemos dos operaciones especiales.
"""
x = 7
y = 3
print(x//y) #cociente
print(x%y) #residuo
```

    2
    1
    


```python
"""
Algunas operaciones en Python están sobre cargadas. Por ejemplo, podemos sumar
cadenas
"""
saludo = "Hola "
nombre = "(Escribe aquí tu nombre)!"
print(saludo+nombre)
```

    Hola (Escribe aquí tu nombre)!
    


```python
"""
Sin embargo, no es así con todas las operaciones
"""
saludo = "Hola "
nombre = "Fulanito!"
try: #Intentaremos...
  print(saludos-nombre) #Restar dos cadenas de caracteres
except: #Si no funciona...
  print("No puedo restar cadenas de caracteres") #Imprimimos un error

```

    No puedo restar cadenas de caracteres
    

### Funciones
Ahora, aprenderemos a crear funciones. Estas nos permitirán reutilizar el código, optimizando nuestro tiempo de desarrollo y haciendo más entendible nuestro procedimiento.


```python
"""
Vamos a *def*inir una función que acepte un nombre (cadena de caracteres) y 
regrese un saludo cordial
"""
def saluda_a(nombre):
  return "Hola "+nombre+"!"

# ahora vamos a ingresar un nombre, guardar el resultado e imprimirlo en pantalla
resultado = saluda_a("Fulanito")
print(resultado)

# Intenta ahora ingresando tu nombre e imprimiendo tu resultado en pantalla
```

    Hola Fulanito!
    


```python
"""
Definamos ahora una función que nos regrese el cociente de una división de enteros
"""
def cociente(p,q):
  return p//q

# probemos con un par de números
print(cociente(7,3))

#ahora intenta algo similar para el residuo
```

    2
    

**¡Excelente!** Hemos terminado con los conceptos más básicos para comenzar a 
programar en Python. Pero antes, vamos a practicar con una lista de ejercicios.

Al final, vamos dejarte las respuestas, pero recuerda, *¡la práctica hace al 
maestro!*
