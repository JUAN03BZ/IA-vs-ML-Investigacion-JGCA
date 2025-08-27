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

print("\n=== Arreglos especiales ===")
mat_ceros = np.zeros((2, 5))   # Matriz 2x5 de ceros
mat_unos = np.ones((3, 3))     # Matriz 3x3 de unos
mat_full = np.full((2, 2), 7)  # Matriz 2x2 con el valor 7

```python
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