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
-----------------------____________________________________-----------------------------------------

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
-----------------------____________________________________-----------------------------------------

Creación y manipulación de DataFrames y series - Cristhian Felipe Bolivar

# C) pandas – Creación y manipulación de DataFrames y series
## Introduccion
Pandas es una libreria de Python, que permite leer y escribir facilmente en formato **CVS**, **Exel** y **SQL**.
## 1- Series
Es parecida a una columna de una tabla en exel, conteniendo una lista de datos con un indice.
- Ejemplo
```python
import pandas as pd

# 1. CREAR UNA SERIE
serie = pd.Series([10, 20, 30, 40], index=["a", "b", "c", "d"])
print("1. Serie:")
print(serie)
print("\n")
```
- Nos imprime en pantalla
```python
Serie:
a    10
b    20
c    30
d    40
dtype: int64
```
## 2- DataFrame
Es una tabla completa como una hoja de exel, siendo esta formada por varias series organizadas en filas y columnas.
- Ejemplo
```python
# 2. CREAR UN DATAFRAME
data = {
    "Nombre": ["Cristhian", "Juan Jose", "Canasto", "German"],
    "Edad": [20, 21, 23, 26],
    "Municipio": ["Tabio", "Cajica", "Chia", "Tocancipa"]
}
df = pd.DataFrame(data)
print("2. DataFrame:")
print(df)
print("\n")
```
- Nos imprime en pantalla
```python
2. DataFrame:
      Nombre  Edad  Municipio
0  Cristhian    20      Tabio
1  Juan Jose    21     Cajica
2    Canasto    23       Chia
3     German    26  Tocancipa
```
## 3- Carga de datos
La libreria pandas permite importar datos de manera sencilla provenientes de archivos **CVS**, **Exel** y **Json**.
- Ejemplo
Previamente se guardo el anterior DataFrame con la siguiente secuencia de codigo con el nombre "personas"
```python
df.to_csv("personas.csv", index=False)
```
Ahora si se carga el DataFrame
```python
# 3. CARGA DE DATOS
df_cargado = pd.read_csv("personas.csv")
print("3. Carga de datos desde CSV:")
print(df_cargado)
print("\n")
```
- Nos imprime en pantalla
```python
3. Carga de datos desde CSV:
      Nombre  Edad  Municipio
0  Cristhian    20      Tabio
1  Juan Jose    21     Cajica
2    Canasto    23       Chia
3     German    26  Tocancipa
```
## 4- Seleccion de columnas 
En Pandas puedes extraer una o varias columnas de un DataFrame  
- Ejemplo
```python
# 4. Selección de columnas
df_cargado = pd.read_csv("personas.csv")
print("Columna Nombre:")
print(df["Nombre"])

print("\nColumnas Nombre y Edad:")
print(df[["Nombre", "Edad"]])
```
- Nos imprime en pantalla
```python
Columna Nombre:
0    Cristhian
1    Juan Jose
2      Canasto
3       German
Name: Nombre, dtype: object

Columnas Nombre y Edad:
      Nombre  Edad
0  Cristhian    20
1  Juan Jose    21
2    Canasto    23
3     German    26

```
## 5- Tipos de datos
Cada columna del DataFrame tiene su propio tipo de dato, estos son float, int, bool, datetime64[ns], timedelta[ns] y object.
-  Ejemplo
```python
# 5. Tipos de datos
df_cargado = pd.read_csv("personas.csv")
for columna in df.columns:
    print(f"La columna '{columna}' es de tipo {df[columna].dtype}")
```
- Nos imprime en pantalla
```python
La columna 'Nombre' es de tipo object
La columna 'Edad' es de tipo int64
La columna 'Municipio' es de tipo object
```

-----------------------____________________________________-----------------------------------------

D-pandas-avanzado - German Bautista 


# Pandas
## Operaciones avanzadas en DataFrames

- Pandas es una librería para manipulación y análisis de datos, basada en DataFrames y Series.

## 1. Filtros

- Filtrar filas de un DataFrame según condiciones.

- Funcion "df[condición]"

- Las operaciones lógicas en Pandas facilitan la combinación de varias condiciones de filtrado con el fin de extraer subconjuntos específicos de un DataFrame, utilizando operadores como & (AND), | (OR) y ~ (NOT).

## Ejemplo

```python
 
import pandas as pd

df = pd.DataFrame({
    'Nombre': ['Ana', 'Luis', 'María', 'Pedro'],
    'Edad': [23, 34, 29, 40],
    'Ciudad': ['Bogotá', 'Medellín', 'Cali', 'Bogotá'],
    'Salario': [2500, 3000, 2800, 4000]
})

# Filtro simple
print(df[df['Edad'] > 30])

# Filtro múltiple (AND)
print(df[(df['Edad'] > 25) & (df['Ciudad'] == 'Bogotá')])

# Filtro múltiple (OR)
print(df[(df['Ciudad'] == 'Bogotá') | (df['Ciudad'] == 'Cali')])
```
## 2. Agrupamiento (GroupBy)

- Permite resumir datos por categorías.

- Funcion df.groupby

## Ejemplo

```python

# Promedio de salario por ciudad
print(df.groupby('Ciudad')['Salario'].mean())

# Varias estadísticas
print(df.groupby('Ciudad')['Edad'].agg(['mean', 'max', 'min']))

```
## 3. Merge / Join

- Combinar DataFrames, similar a JOIN en SQL.

- Funcion pd.DataFrame()

## Ejemplo

```python

df1 = pd.DataFrame({'ID':[1,2,3], 'Nombre':['Ana','Luis','María']})
df2 = pd.DataFrame({'ID':[1,2,4], 'Ciudad':['Bogotá','Medellín','Cali']})

# Inner Join (solo coincidencias)
print(pd.merge(df1, df2, on='ID', how='inner'))

# Left Join (todos los de df1)
print(pd.merge(df1, df2, on='ID', how='left'))

# Outer Join (todos, incluso sin coincidencia)
print(pd.merge(df1, df2, on='ID', how='outer'))

```
## 4. Manejo de Valores Nulos

- Trabajar con datos incompletos.

- funcion dropna(), fillna(), isnull()

## Ejemplo

```python

df_null = pd.DataFrame({
    'A': [1, 2, None, 4],
    'B': [5, None, None, 8]
})

print(df_null.isnull())    # Detectar nulos
print(df_null.dropna())    # Eliminar filas con nulos
print(df_null.fillna(0))   # Rellenar con 0
print(df_null.fillna(df_null.mean())) # Rellenar con promedio

```
## 5. Exportación / Importación

- Guardar y cargar datos en distintos formatos.

- Funcion Exportacion to_csv(), to_excel(), to_json()

- Funcion Importacion read_csv(), read_excel(), read_json()

## Ejemplo

```python

# CSV
df.to_csv('datos.csv', index=False)
df_csv = pd.read_csv('datos.csv')

# Excel
df.to_excel('datos.xlsx', index=False)
df_xls = pd.read_excel('datos.xlsx')

# JSON
df.to_json('datos.json', orient='records')
df_json = pd.read_json('datos.json')

```