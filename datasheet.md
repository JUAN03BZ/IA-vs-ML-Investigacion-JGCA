# Pandas
## Operaciones avanzadas en DataFrames

- Pandas es una librería para manipulación y análisis de datos, basada en DataFrames y Series.

## 1. Filtros

- Filtrar filas de un DataFrame según condiciones.

- Funcion "df[condición]"

- Las operaciones lógicas en Pandas facilitan la combinación de varias condiciones de filtrado con el fin de extraer subconjuntos específicos de un DataFrame, utilizando operadores como & (AND), | (OR) y ~ (NOT).


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

```python

# Promedio de salario por ciudad
print(df.groupby('Ciudad')['Salario'].mean())

# Varias estadísticas
print(df.groupby('Ciudad')['Edad'].agg(['mean', 'max', 'min']))

```
## 3. Merge / Join

- Combinar DataFrames, similar a JOIN en SQL.

- Funcion pd.DataFrame()

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
