# A) NumPy – Creación y manipulación de arreglos

## Introducción
**NumPy** (Numerical Python) es una librería fundamental para el análisis numérico en Python.  
Permite trabajar con **arreglos multidimensionales** de manera eficiente y ofrece funciones matemáticas optimizadas para cálculos científicos.

---

## 1. Creación de Arreglos
Con `np.array()` podemos construir arreglos a partir de listas o tuplas.
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