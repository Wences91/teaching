# Introducción al manejo de datos en Python 🐍
---
**Sobre el curso:** Este curso tiene por finalidad el aprendizaje práctico de Python orientado al manejo básico y sencillo de datos.

# **Sesión 2: Manejo básico de datos en Python** 

En esta segunda sesión, vamos a importar y trabajar con Pandas para explorar sus funcionalidades básicas.

## **1. Importar Pandas**
Una vez instalado, podemos importar Pandas para comenzar a trabajar con datos:
```python
import pandas as pd
```

## **2. Importar datos**
Pandas soporta la lectura de una variedad de formatos de archivos como CSV, Excel entre otros. El método `read_csv` es frecuentemente usado:
```python
df = pd.read_csv('ruta/al/archivo.csv', sep=',', header=0)
```
**Parámetros principales:**
- `filepath_or_buffer`: Ruta del archivo o un objeto similar a un archivo que contiene los datos.
- `sep`: el delimitador del archivo (por defecto, `,`).
- `header`: índice de la fila que se usa como cabecera.
- `skiprows`: Número de filas o lista de números de línea para omitir al leer el archivo.
- `na_values`: Secuencia de valores que, si se encuentran en el archivo, deben ser tratados como NaN.
- `dtype`: Tipo de datos para las columnas. Por ejemplo, {'a': np.float64, 'b': np.int32}.
- `encoding`: Codificación del archivo (generalmente UTF-8).

### **3. Previsualización de datos**
Para obtener una vista rápida de los datos, podemos utilizar:
```python
df.head()  # Muestra las primeras 5 filas
```

También puede usar:
- `head()`, `tail()`: Muestra las primeras o últimas 'n' filas.
- `describe()`: Proporciona estadísticas descriptivas resumidas.
- `info()`: Resumen conciso del DataFrame, incluyendo el tipo de datos de las columnas y los valores no nulos.
- `dtypes`: Muestra los tipos de datos de cada columna.
- `value_counts()`: Cuenta cuántas veces aparece cada valor único en una columna.

### **4. Seleccionar columnas**
Para seleccionar una sola columna, utilizamos:
```python
columna = df['NombreColumna']
```

### **5. Seleccionar filas por índice**
Podemos seleccionar filas específicas usando su índice:
```python
filas = df.iloc[0:5]  # Selecciona las primeras 5 filas
```

### **6. Seleccionar filas usando condiciones**
También podemos seleccionar filas que cumplan una condición:
```python
condicion = df[df['Edad'] > 30]  # Selecciona filas donde la columna 'Edad' es mayor que 30
```

### **7. Exportar a CSV**
Para exportar un DataFrame a CSV, utilizamos:
```python
df.to_csv('ruta/al/nuevo_archivo.csv', index=False)
```
**Parámetros principales:**
- `index`: indica si incluir el índice de las filas en el archivo.
- `sep`: el delimitador del archivo (por defecto, `,`).
- `encoding`: Codificación del archivo (generalmente UTF-8).

---
# Información
<div class="alert alert-block alert-info">
    <b>Autor:</b> Wenceslao Arroyo-Machado</br>
    <b>Fecha de actualización:</b> 26/04/2024</br>
    <b>GitHub:</b> <a href="https://github.com/Wences91/teaching">https://github.com/Wences91/teaching</a>
</div>
