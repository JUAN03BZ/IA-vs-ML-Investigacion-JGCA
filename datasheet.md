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