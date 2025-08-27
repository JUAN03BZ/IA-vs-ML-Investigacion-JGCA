# A) NumPy – Creación y manipulación de arreglos

## Introducción
**NumPy** (Numerical Python) es una librería fundamental para el análisis numérico en Python.  
Permite trabajar con **arreglos multidimensionales** de manera eficiente y ofrece funciones matemáticas optimizadas para cálculos científicos.

---

## 1. Creación de Arreglos
Un arreglo en NumPy se puede construir a partir de listas o tuplas utilizando la función `np.array()`.  
Esto permite transformar estructuras tradicionales de Python en **estructuras más eficientes** para cálculos numéricos.

- Ejemplo
```python
import numpy as np

print("=== Creación de Arreglos ===")
arr1 = np.array([2, 4, 6, 8])
print("Arreglo desde lista:", arr1)

arr2 = np.array((1, 3, 5))
print("Arreglo desde tupla:", arr2)
```
- Nos devuelve como resultado

```python
=== Creación de Arreglos ===
Arreglo desde lista: [2 4 6 8]
Arreglo desde tupla: [1 3 5]
```
## 2. Matrices de ceros, unos y valores constantes

NumPy incluye funciones especiales para crear matrices inicializadas automáticamente.
Estas funciones son útiles cuando necesitamos espacios predefinidos para cálculos, como por ejemplo en redes neuronales, simulaciones o inicialización de datos.

- np.zeros((m, n)) → Crea una matriz de tamaño m x n llena de ceros.
- np.ones((m, n)) → Crea una matriz de tamaño m x n llena de unos.
- np.full((m, n), valor) → Crea una matriz de tamaño m x n con un valor constante.

```python
print("\n=== Arreglos especiales ===")
mat_ceros = np.zeros((2, 5))   # Matriz 2x5 de ceros
mat_unos = np.ones((3, 3))     # Matriz 3x3 de unos
mat_full = np.full((2, 2), 7)  # Matriz 2x2 con el valor 7

print("Matriz de ceros:\n", mat_ceros)
print("Matriz de unos:\n", mat_unos)
print("Matriz con valor fijo:\n", mat_full)
```
- Nos devuelve como resultado

```python
=== Arreglos especiales ===
Matriz de ceros:
 [[0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0.]]
Matriz de unos:
 [[1. 1. 1.]
 [1. 1. 1.]
 [1. 1. 1.]]
Matriz con valor fijo:
 [[7 7]
 [7 7]]
```

## 3. Operaciones entre arreglos

Una de las ventajas más importantes de NumPy es que permite realizar operaciones matemáticas vectorizadas directamente entre arreglos.
Esto significa que no necesitamos usar bucles for para aplicar operaciones a cada elemento: NumPy lo hace de forma automática y optimizada.

- Ejemplo

```python
print("\n=== Operaciones con arreglos ===")
x = np.array([5, 10, 15])
y = np.array([2, 4, 6])

print("Arreglo x:", x)
print("Arreglo y:", y)
print("Suma:", x + y)
print("Resta:", x - y)
print("Potencia:", x ** 2)
```

- Nos devuelve como resultado

```python
=== Operaciones con arreglos ===
Arreglo x: [ 5 10 15]
Arreglo y: [2 4 6]
Suma: [ 7 14 21]
Resta: [3 6 9]
Potencia: [ 25 100 225]
```

## 4. Estadísticos básicos

NumPy también incluye funciones para calcular estadísticas de manera directa.
Esto simplifica tareas comunes como obtener promedio, desviación estándar, valores máximos y mínimos, sin necesidad de escribir código adicional.

- Ejemplo

```python
print("\n=== Estadísticos básicos ===")
valores = np.array([12, 7, 9, 15, 21])

print("Datos:", valores)
print("Media:", np.mean(valores))
print("Desviación estándar:", np.std(valores))
print("Máximo:", np.max(valores))
print("Mínimo:", np.min(valores))
```

- Nos devuelve como resultado

```python
=== Estadísticos básicos ===
Datos: [12  7  9 15 21]
Media: 12.8
Desviación estándar: 4.632493928760187
Máximo: 21
Mínimo: 7
```

## 5. np.arange y np.linspace

NumPy ofrece funciones para generar secuencias numéricas de forma sencilla:

- np.arange(inicio, fin, paso) → genera valores con un incremento definido.
- np.linspace(inicio, fin, num) → genera un número de valores igualmente espaciados en un rango.

```python
print("\n=== Rango de valores ===")
r1 = np.arange(1, 11, 2)   # 1 a 9 con paso de 2
r2 = np.linspace(0, 5, 6)  # 6 valores de 0 a 5

print("np.arange(1, 11, 2):", r1)
print("np.linspace(0, 5, 6):", r2)
```
- Nos devuelve como resultado

```python
=== Rango de valores ===
np.arange(1, 11, 2): [1 3 5 7 9]
np.linspace(0, 5, 6): [0. 1. 2. 3. 4. 5.]
```

## 6. Propiedades de un arreglo

Cada arreglo en NumPy tiene propiedades que describen sus características:

- .shape → número de filas y columnas del arreglo.
- .size → cantidad total de elementos.
- .dtype → tipo de datos que contiene.


-Ejemplo

```python
print("\n=== Propiedades del arreglo ===")
m = np.array([[2, 4], [6, 8], [10, 12]])

print("Arreglo:\n", m)
print("Forma (shape):", m.shape)
print("Elementos totales (size):", m.size)
print("Tipo de dato (dtype):", m.dtype)
```
- Nos devuelve como resultado

```python
=== Propiedades del arreglo ===
Arreglo:
 [[ 2  4]
 [ 6  8]
 [10 12]]
Forma (shape): (3, 2)
Elementos totales (size): 6
Tipo de dato (dtype): int64
```