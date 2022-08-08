# Técnicas de búsqueda bibliográficas para la investigación
---

<div class="alert alert-secondary" role="alert">
  <b>Contenido</b>: Descripción del proceso de consulta en bases de datos bibliográficas. Se presta especial atención a la selección de bases de datos bibliográficas y la elaboración de la ecuación de búsqueda.
</div>

# 1. El proceso de búsqueda
La busqueda en bases de datos bibliográficas es el punto de partida de toda investigación. Estas herramientas no incluyen en sus bases de datos documentos, en su lugar tienen registro bibliográficos. Un registro bibliográfico es un **conjunto de metadatos** en un formato estándar que representa un documento y permiten su correcta identificación.

Ejemplo de un registro bibliográfico en [Dialnet](https://dialnet.unirioja.es/servlet/articulo?codigo=8518846).
![Registro en Dialnet](https://raw.githubusercontent.com/Wences91/teaching/main/images/te%CC%81cnicas_bu%CC%81squeda_bibliogra%CC%81fica/registro_dialnet.jpg)

La búsqueda de registros bibliográficos, y la de cualquier tipo de información, involucra de manera general dos procesos:
+ Definir la necesidad informativa
+ (Re)Elaboración de la consulta
+ Exportación de los resultados

# 2. Definir la necesidad informativa
La delimitación de la necesidad informativa es el primer paso. Este es el único elemento que debemos tener claramente establecido desde el inicio y que, dentro del resto de pasos de este proceso, **no se verá alterado**. *¿Cuál es nuestro problema de investigación concreto?* De igual manera, también se debe tener claro el objetivo de dichos registros. *¿Queremos usar los registros para elaborar un estado del arte o para llevar a cabo un análisis bibliométrico?*

Este es el pilar de nuestra búsqueda. Es posible que no sepamos en este momento dónde vamos a buscar o cuáles son los mejores términos a usar en la consulta, pero siempre debemos tener claro que queremos localizar en última instancia y para qué.

# 3. (Re)Elaboración de la consulta
Hay varios aspectos importantes a tener en cuenta para evitar pasar por alto registros de interés para nuestra necesidad o la introducción de mucho ruido.

Un **marco de búsqueda** general debe contemplar los siguientes apartados[[1]](#1), los cuales constituyen un **ciclo** y pueden sufrir cambios durante el proceso de búsqueda:
1. Selección de la base de datos
2. Elaboración de la ecuación de búsqueda
3. Depuración de la consulta

## 3.1. Selección de la base de datos
Afortunadamente, nos encontramos en un escenario repleto de herramientas para la búsqueda de registros bibliográficos [[2]](#2). Si bien este terreno es algo convulso, lo cierto es que hay herramientas para todo tipo de problemas y muchas de ellas son de acceso gratuito.

Debido a esta extensa oferta, resulta crucial conocer varios aspectos de ellas:
+ **Cobertura**: Uno de los principales elementos diferenciadores de las bases de datos bibliográficas es el número de documentos que tiene indexados [[3]](#3). Aunque es un importante reclamo y aspecto a tener en cuenta, **no tiene por qué ser el criterio principal** a la hora de escoger.
+ **Sesgos**: Son múltiples los sesgos que puede tener una base de datos (tipología, temática[[4]](#4), cobertura temporal, enfoque internacional...). Identifica cuál es el sesgo o sesgos de la base de datos. Las **bases de datos multidisciplinares** son fundamentales y se adaptan a la mayoría de casuísticas, pero en casos concretos son insuficientes por dichos motivos.
+ **Curación y normalización**: A nivel práctico, son muy diferenciadores los trabajos realizados en materia de curación y normalización de los registros y sus metadatos (materias, autores, instituciones...). Web of Science y Scopus son claros ejemplos de ello.
+ **Metadatos** (para análisis bibliométricos): Todas las bases de datos bibliográficas cuentan, o deben contar, con opciones de exportación de registros bibliográficos. En especial en los formatos de archivo estándar de referencias bibliográficas: *bib* y *ris*. Pero si el objetivo es llevar a cabo un análisis bibliométrico conviene asegurar que en este u otros formatos se incluyen los metadatos que queremos analizar (por ejemplo, palabras clave o materías, referencias citadas...). En este sentido, son de cada vez mayor importancia las APIs[[5]](#5).

## 3.2. Elaboración de la ecuación de búsqueda
Una vez identificada nuestra necesidad y la base de datos a emplear, toca elaborar una ecuación de búsqueda[[6]](#6). Con independencia de la base de datos escogida el proceso general es el mismo y el lenguaje puede tener pequeñas diferencias en el uso de algunos operadores u opciones de búsqueda.

### 3.2.1. Los operadores
En su gran mayoría, las consultas contienen diferentes elementos, más allá de unos términos, y son varios los operadores que entran en juego[[7]](#7). Para elaborar dicha consulta existe todo un lenguaje en el que casi siempre vas a encontrar:

+ **Operadores de campo**: Permiten indicar el campo exacto del regisro bibliográfico en el que se busca un término. Aunque pueden existir elementos comunes, cada buscador dispone de campos especificos.
+ **Operadores booleanos**: Común a casi todos los buscadores, permiten combinar operadores de campo y términos de búsqueda. Es crucial dominarlos.
+ **Otros operadores comunes**: Junto a los booleanos, la mayoría suelen permitir su uso.

Los operadores booleanos están basados en el álgebra de Boole y permite hacer búsquedas precisas indicando en nuestra ecuación de consulta cómo han de combinarse dos o más elementos de la misma. Los operadores básicos son tres:
* **OR** - Booleano de **unión**. Devuelve registros que cumplan uno o ambos criterios. Búsquedas poco restrictivas.
* **AND** - Booleano de **intersección**. Devuelve solo los registros que cumplen ambos criterios. Búsquedas restrictivas.
* **NOT** - Booleano de **exclusión**. Devuelve los registros que cumplen el primer critero pero no el segundo. Búsquedas restrictivas.

Operadores booleanos OR, AND y NOT
![Álgebra de Boole](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/boole.png)

Hay una gran cantidad de operadores más allá de los booleanos. A destacar las comillas dobles ("") para hacer búsquedas de términos exactos y el asterisco (\*) para el truncamiento. 

### 3.2.2. La búsqueda
La mayoría de bases de datos bibliográficas disponen de dos tipos de búsquedas:
* **Búsqueda simple**
* **Búsqueda avanzada**
* **Búsqueda en API**

Por defecto, veremos en la mayoría de ocasiones la búsqueda simple al entrar en las bases de datos bibliográficas. Esta es una busqueda más guiada, en la que la interfaz nos facilita la consulta mediante opciones interactivas, por ejemplo con diferentes cajas de búsqueda para cada campo de búsqueda y la posibilidad de seleccionar con un click el operador booleano que los conecta. La búsqueda avanzada consiste en una única caja de consulta en la que se introduce la ecuación de consulta completa incluyendo tanto los campos y términos como los operadorer. Fuera de la interfaz de la aplicación web se encuentran las APIs, en las cuales se pueden llevar búsquedas mucho más precisas y aplicando la misma ecuación que en la avanzada.

Diferencia entre la búsqueda simple y avanzada en Scopus
![Búsqueda simple y avanzada](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/busqueda_simple_avanzada.png)

### 3.2.3. Elementos a tener en cuenta
Hay que realizar varias consideracion en la búsqueda:
1. Campos como los autores, nombre de institución o las categorías, suelen disponen de un índice o lenguaje controlado.
2. En la mayoría de los casos va a ser necesario delimitar temporalmente los registros.
3. Al fijar un área **temática** no confundas la búsqueda en palabras clave con la clasificación temática de la base de datos.


### 3.3. Depuración de la consulta




# Referencias
<a id="1">[1]</a>  Codina, L. (2019, noviembre 7). Revisiones sistematizadas para trabajos académicos · Fases de Búsqueda y Evaluación. *Lluís Codina*. https://www.lluiscodina.com/revisiones-sistematizadas-busqueda-evaluacion/

<a id="2">[2]</a>  List of academic databases and search engines. (2022). En *Wikipedia*. https://en.wikipedia.org/w/index.php?title=List_of_academic_databases_and_search_engines&oldid=1101901386

<a id="3">[3]</a>  Visser, M., van Eck, N. J., & Waltman, L. (2021). Large-scale comparison of bibliographic data sources: Scopus, Web of Science, Dimensions, Crossref, and Microsoft Academic. *Quantitative Science Studies*, 2(1), 20-41. [https://doi.org/10.1162/qss_a_00112](https://doi.org/10.1162/qss_a_00112)

<a id="4">[4]</a> Gusenbauer, M. (2022). Search where you will find most: Comparing the disciplinary coverage of 56 bibliographic databases. Scientometrics, 127(5), 2683-2745. https://doi.org/10.1007/s11192-022-04289-7

<a id="5">[5]</a> Torres-Salinas, D., & Arroyo-Machado, W. (2022). APIs en contextos bibliométricos: Introducción básica y corpus exhaustivo. Anuario ThinkEPI, e16a09. https://doi.org/10.3145/thinkepi.2022.e16a09

<a id="6">[6]</a> Alba-Ruiz, R. (2020). *Aprender a elaborar ecuaciones de búsqueda bibliográficas*. https://www.youtube.com/watch?v=m0Rrl2qTUZc

<a id="7">[7]</a> Arroyo-Machado, W. (2022). Introducción a las principales bases de datos bibliométricas (Web of science y scopus). HackMD. https://hackmd.io/@Wences/2_introducci%C3%B3n_bibliometr%C3%ADa

---

# Información
<div class="alert alert-block alert-info">
    <b>Autor:</b> <a href="https://orcid.org/0000-0001-9437-8757">Wenceslao Arroyo-Machado</a></br>
    <b>Fecha de actualización:</b> 08/08/2022</br>
    <b>GitHub:</b> <a href="https://github.com/Wences91/teaching">https://github.com/Wences91/teaching</a>
</div>