
Operaciones estadisticas y funciones avanzadas - Andres Canasto

# Operaciones estadisticas y funciones avanzadas

Esta sección muestra ejemplos de uso de funciones estadísticas y avanzadas de la librería **NumPy**, ejecutados en Google Colab.

## 1. Promedio (np.mean)

- Ejemplo

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print("Arreglo:", arr)
print("Promedio:", np.mean(arr))

```
**Resultado**

```python
Arreglo: [1 2 3 4 5]
Promedio: 3.0
```

## 2. Desviación estándar (np.std)

- Ejemplo

```python
print("Desviación estándar:", np.std(arr))
```

**Resultado**

```python
Desviación estándar: 1.4142135623730951
```

##  3. Suma (np.sum)

- Ejemplo

```python
print("Suma de elementos:", np.sum(arr))
```

**Resultado**

Suma de elementos: 15

## 4. Creacion de Secuencias (np.arange)

- Ejemplo

```python
secuencia = np.arange(0, 10, 2)  # desde 0 hasta 10 (excluido) con paso 2
print(secuencia)
```

**Resultado**

```python
[0 2 4 6 8]
```


## 5. Numeros Espaciados (np.linspace)

- Ejemplo

```python
espaciado = np.linspace(0, 1, 5)  # 5 números entre 0 y 1
print(espaciado)
```
**Resultado**

[0.   0.25 0.5  0.75 1.  ]

## 6. Aleatorios (np.random.rand)

- Ejemplo

```python
aleatorios = np.random.rand(3, 3)  # matriz 3x3 con números aleatorios [0,1)
print(aleatorios)
```
**Resultado**

```python
Producto matricial:
 [[19 22]
 [43 50]]
```

Como conclusion, es que trabajar con las funciones estadísticas y avanzadas de NumPy es súper útil porque nos ahorra tiempo y esfuerzo al hacer cálculos que de otra forma serían largos o complicados. Con unos pocos comandos podemos sacar promedios, desviaciones, sumar datos, crear secuencias o hasta generar números aleatorios para hacer pruebas. Además, con las operaciones de álgebra lineal como el producto de matrices, se pueden resolver problemas que son la base de muchas aplicaciones modernas como la inteligencia artificial o el análisis de grandes volúmenes de datos.
En pocas palabras, NumPy nos da las herramientas necesarias para trabajar con datos de forma rápida, sencilla y muy eficiente
