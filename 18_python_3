# Introducción al manejo de datos en Python 🐍
---
**Sobre el curso:** Este curso está diseñado para fomentar el aprendizaje práctico de Python, con un enfoque en operaciones avanzadas de manejo de datos utilizando Pandas.

# **Sesión 3: Operaciones avanzadas en Pandas**

Esta sesión cubre técnicas principales de Pandas, incluyendo joins, búsqueda de cadenas, agregación de datos y visualizaciones.

## **1. Combinación de DataFrames**
Los joins son esenciales para combinar DataFrames en base a una o más claves con `merge()`. El parámetro `how` indica cómo se hará el join (left, right, inner o outer).

```python
# Inner Join
df_inner = pd.merge(df1, df2, on='key', how='inner')
```

## **2. Búsqueda de cadenas de texto**
Pandas permite la búsqueda dentro de series de texto usando métodos como `str.contains()`.


```python
# Filtrar filas que contienen una cadena específica
df[df['column'].str.contains('texto buscado')]
```

Este método es compatible con expresiones regulares para búsquedas complejas en textos.

```python
# Filtrar utilizando una expresión regular
df[df['column'].str.contains(r'^[A-Za-z]+$', regex=True)]
```

## **3. Agregación de datos**
Una función básica es la del recuento de ocurrencia de valores únicos dentro de una columna con `value_counts()`.

```python
# Contar valores únicos
df['column'].value_counts()
```

Sin embargo, Pandas también permite realizar operaciones de agregación para resumir datos a través de `groupby()`.

```python
# Agregación simple por grupo
grouped_data = df.groupby('group_key').sum()
```

Además, se pueden especificar varias operaciones de manera simultánea con `agg()`.

```python
# Uso de agg() para múltiples operaciones
df.groupby('group_key').agg({'column1': 'sum', 'column2': 'mean'})
```

## **4. Visualización de datos**
Pandas tiene integrado Matplotlib, que permite crear una variedad de gráficos para analizar los datos visualmente de manera sencilla.

```python
# Gráfico de barras
df['column'].value_counts().plot(kind='bar')

# Gráfico de líneas
df.plot(kind='line')

# Histograma
df['column'].plot(kind='hist', bins=20)

# Scatter plot
df.plot(kind='scatter', x='column1', y='column2')

# Gráfico de boxplot
df.plot(kind='box')
```

---
# Información
<div class="alert alert-block alert-info">
    <b>Autor:</b> Wenceslao Arroyo-Machado</br>
    <b>Fecha de actualización:</b> 03/05/2024</br>
    <b>GitHub:</b> <a href="https://github.com/Wences91/teaching">https://github.com/Wences91/teaching</a>
</div>
