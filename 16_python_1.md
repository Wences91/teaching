# Introducción al manejo de datos en Python 🐍
---
**Sobre el curso:** Este curso tiene por finalidad el aprendizaje práctico de Python orientado al manejo básico y sencillo de datos.

# **Sesión 1: Introducción a Python y notebooks** 
En esta primera sesión, vamos a establecer las bases necesarias para que puedas comenzar a explorar y manipular datos en sesiones posteriores utilizando Pandas, una herramienta poderosa en el campo de la ciencia de datos.

## **1. Introducción a Python**
Python es un lenguaje de programación de alto nivel que se ha hecho muy popular debido a su simplicidad y flexibilidad. Es especialmente valorado en áreas como análisis de datos, aprendizaje automático, desarrollo web, y automatización de tareas mediante scripts.

Los principales factores para su popularidad son:
- **Fácil de aprender:** Sintaxis clara y legible.
- **Versátil:** Desde scripts simples hasta sistemas complejos.
- **Comunidad grande:** Una comunidad activa con una amplia gama de recursos y paquetes.

Este es un pequeño ejemplo de código en Python:
```python
# Esto es un comentario en Python
print("Lo primero de todo, ¿cómo están los máquinas?")
```

## **2.Entorno de programación**
Un Entorno de Desarrollo Integrado (IDE en inglés) es una aplicación que proporciona facilidades a los programadores para el desarrollo de software. Aquí hay algunos entornos y herramientas donde puedes escribir y ejecutar código Python. Los principales IDE o ecosistemas para ello son:

| Herramienta       | Descripción                                          | Tipo      |
|-------------------|------------------------------------------------------|-----------|
| Visual Studio Code| Editor de código ligero pero potente                 | IDE       |
| Anaconda          | Distribución de Python y R que incluye bibliotecas   | Plataforma|
| Google Colab      | Entorno en la nube que facilita el trabajo colaborativo | Notebook  |
| Spyder            | IDE orientado a la ciencia de datos                  | IDE       |

- **Visual Studio Code** es flexible y configurable con extensiones para Python.
- **Anaconda** simplifica la gestión de paquetes y entornos virtuales, ideal para ciencia de datos.
- **Google Colab** ofrece un entorno de notebooks en la nube con recursos gratuitos de computación.
- **Spyder** está diseñado específicamente para científicos de datos y ofrece integración directa con bibliotecas de análisis de datos.

## **3. Fundamentos de Python**
Para aprender Python en profundidad y de base, es necesaria una mayor dedicación. Estos son algunos cursos recomendados para personas que vayan a comenzar desde cero:
- [Learn Python](https://www.learnpython.org/)
- [Python for beginners](https://learn.microsoft.com/en-us/training/paths/beginner-python/)
- [Code in Place](https://codeinplace.stanford.edu/)


### **3.1. Variables y tipos de datos**
Es fundamental entender cómo almacenar y manipular datos en Python:
- **Variables**: Contenedores para almacenar datos. Puedes pensar en ellas **como cajas etiquetadas** donde guardas información.
- **Tipos de datos**: Define la naturaleza de los datos. Python determina los tipos automáticamente. Estos son algunos de los más comunes:

```python
numero = 30  # int
precio = 99.99  # float
nombre = "Ciencia de Datos"  # str
activo = True  # bool
```
### **3.2. Operaciones básicas**
Vamos a explorar cómo realizar cálculos y comparaciones básicas en Python, fundamentales para cualquier análisis de datos.

```python
suma = 50 + 30  # Suma
mayor = 50 > 30  # Comparación
```

### **3.3. Estructuras de datos básicas**
Las estructuras de datos permiten organizar la información de manera que se pueda acceder y modificar de manera eficiente.

```python
# Lista de colores
colores = ["rojo", "verde", "azul"]

# Diccionario con información de un usuario
usuario = {"nombre": "Ana", "edad": 34}
```

### **3.4. Funciones básicas y paquetes**

Las funciones permiten reutilizar código y las bibliotecas extienden las capacidades de Python.

```python
def saludar(nombre):
    return "Hola " + nombre

import math
print(math.sqrt(16))  # Imprime la raíz cuadrada de 16
```
## **4. Paquetes en Python**
Los paquetes son colecciones de módulos que otros programadores han creado para expandir las capacidades de Python. Para usar un paquete, generalmente necesitas instalarlo y luego importarlo en tu script.

```python
# Instalación de un paquete desde Jupyter Notebook
!pip install pandas
```

---
# Información
<div class="alert alert-block alert-info">
    <b>Autor:</b> Wenceslao Arroyo-Machado</br>
    <b>Fecha de actualización:</b> 12/04/2024</br>
    <b>GitHub:</b> <a href="https://github.com/Wences91/teaching">https://github.com/Wences91/teaching</a>
</div>
