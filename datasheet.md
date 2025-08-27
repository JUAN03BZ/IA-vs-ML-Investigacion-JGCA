# Pandas
## Operaciones avanzadas en DataFrames

- Pandas es una librería para manipulación y análisis de datos, basada en DataFrames y Series.

## 1. Filtros
- Filtrar filas de un DataFrame según condiciones.

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
## 2.Agrupamiento (GroupBy)

- Permite resumir datos por categorías.

```python

# Promedio de salario por ciudad
print(df.groupby('Ciudad')['Salario'].mean())

# Varias estadísticas
print(df.groupby('Ciudad')['Edad'].agg(['mean', 'max', 'min']))

```

