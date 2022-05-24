# Introducción a las principales bases de datos bibliométricas (Web of Science y Scopus)

## 1. Lenguaje de consulta
Es crucial en un análisis bibliométrico realizar una correcta búsqueda. Pese a las facilidades que ofrecen muchas de las interfaces de búsqueda de las bases de datos bibliográficas, este proceso requiere especial atención. Una incorrecta búsqueda puede conducir a datos con mucho ruido, poco o demasiado exhaustivos...

### 1.1. El proceso de búsqueda
De manera general el proceso de búsqueda plantea los siguientes pasos:
1. **¿Qué quieres buscar?** - Elaboración de una pregunta
2. **¿Dónde vas a buscar?** - Selección de una base de datos (cobertura, sesgo, especialización...)
3. **Consulta** - Construcción de la búsqueda
4. **Depura la consulta** - Ajuste y repetición de la consulta

Resueltos los dos primeros pasos llega el turno de la consulta en la base de datos. Esta precisa de una correcta estrategia y por lo general requiere de varios intentos, pruebas y comprobaciones antes de dar con la más adecuada. **Nunca te conformes a la primera**.

No va a ser lo habitual que nuestra **ecuación de consulta** esté conformada de un único término o campo de búsqueda, suelen intervenir diferentes elementos. Para elaborar dicha consulta existe todo un lenguaje en el que vas a encontrar:
* **Operadores de campo** - Permiten indicar el campo exacto del regisro bibliográfico en el que se busca un término. Aunque pueden existir elementos comunes, cada buscador dispone de campos especificos.
* **Operadores booleanos** - Común a casi todos los buscadores, permiten combinar operadores de campo y términos de búsqueda. Es crucial dominarlos.
* **Otros operadores comunes** - Junto a los booleanos, la mayoría suelen permitir su uso.

### 1.2. Operadores booleanos
Estos operadores están basados en el álgebra de Boole y permite hacer búsqueda precisas indicando en nuestra ecuación de consulta cómo han de combinarse dos o más elementos de la consulta.

Los operadores básicos son tres:
* **OR** - Booleano de **unión**. Devuelve registros que cumplan uno o ambos criterios. Búsquedas poco restrictivas.
* **AND** - Booleano de **intersección**. Devuelve solo los registros que cumplen ambos criterios. Búsquedas restrictivas.
* **NOT** - Booleano de **exclusión**. Devuelve los registros que cumplen el primer critero pero no el segundo. Búsquedas restrictivas.

Operadores booleanos OR, AND y NOT
![Álgebra de Boole](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/boole.png)

Pero cuidado, aunque se usen en prácticamente casi todos los buscadores, puede haya variaciones en su denominación o que su uso se realice mediante símbolos. Por ejemplo, **NOT** puede aparecer como **-** y **AND** como **&**.

### 1.3. Otros operadores comunes
En línea con los los operadores booleanos existen otros que también suelen ser comunes en los buscadores y que resultan imprescindibles. De manera general se puede destacar:
* **()** - los paréntesis hacen posible agrupar operadores cuando la ecuación de consulta involucra más de uno.

Por otro lado, al introducir términos de busqueda, podemos manipular dichas cadenas para hacerlas más o menos restrictivas con:
* **""** - las comillas permiten buscar cadenas de texto exactas.
* **\*** - gracias al asterisco se puede llevar a cabo el truncamiento de uno o varios caracteres.


## 2. Búsquedas bibliográficas
En este caso la búsqueda está centrada en las dos principales y tradicionales bases de datos bibliográficas: *Web of Science* y *Scopus*. Aunque existe todo un abanico de alternativas y muchos de los aspecto vistos aquí son extrapolables a ellas.

Tabla comparativa de la cobertura de Scopus y Web of Science (Pranckutė, 2021).
![Tabla comparativa de Scopus y Web of Science](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/tabla_comparativa.png)


### 2.1. Primeros pasos
La mayoría de bases de datos bibliográficas disponen de dos tipos de búsquedas:
* **Busqueda simple**
* **Busqueda avanzada**

Por defecto, veremos en la mayoría de ocasiones la búsqueda simple al entrar en las bases de datos bibliográficas. Esta es una busqueda más guiada en la que la interfaz nos facilita la consulta mediante opciones interactivas, por ejemplo con diferentes cajas de búsqueda para cada campo de búsqueda y la posibilidad de seleccionar con el ratón el operador booleano que los conecta. La búsqueda avanzada consiste en una única caja de consulta en la que se introduce la ecuación de consulta completa incluyendo tanto los campos y términos como los operadorer.

Diferencia entre la búsqueda simple y avanzada en Scopus
![Búsqueda simple y avanzada](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/busqueda_simple_avanzada.png)

En el caso concreto de *Web of Science*, se pueden filtrar las bases de datos que se usan en la búsqueda. Presta atención a ello, porque los campos de búsqueda o filtros pueden variar. Por lo general usa la **Web of Science Core Collection**, dentro de la cual puedes seleccionar varias bases de datos en específico, siendo las principales:
* Science Citation Index Expanded (SCI)
* Social Sciences Citation Index (SSCI)
* Arts & Humanities Citation Index (AHCI)
* Emerging Sources Citation Index (ESCI)

### 2.2. Aspectos a tener cuenta
Existen numerosos campos de búsqueda que se pueden emplear, los principales son:
* Tema (Título, resumen o palabras clave)
* Título
* Resumen
* Palabras clave
* Categorías
* Autor
* Editor
* Nombre de publicación
* Fecha de publicación (cuidado con el tipo de fecha)
* Institución
* Dirección

Algunos de estos campos, como la institución o las categorías, disponen de un índice.

Más allá del tipo de búsqueda y la selección correcta de los campos de búsqueda, hay dos aspectos que siempren han de considerarse:
- [x] **Fecha de publicación** - Por norma general, considera solo los años completos y ten en cuenta que análisis quieres realizar para centrar la atención en un periodo más o menos extenso y/o reciente.
- [x] **Tipología documental** - En función del análisis emplea solo aquellas tipologías realmente relevantes.

A la hora de fijar la **temática** no despistes el uso de **categorías** de la base de datos (Categories en *Web of Science*, Subject Areas en *Scopus*). Estas son las que indican que una publicación pertenece a un disciplina concreta. Su uso con la búsqueda de términos (título, abstract y palabras clave) puede generar confusión.

Por ejemplo, para buscar publicaciones de Wikipedia relativas a las Ciencias Sociales tenemos dos opciones:
1. ~~**Palabras clave**: Wikipedia AND "Ciencias Sociales"~~
2. **Palabras clave**: Wikipedia AND **Área**:"Ciencias Sociales"


### 2.3. El filtrado
Con independencia de la búsqueda efectuada, los resultados serán mostrados en una página que nos permite filtrar más los resultados.

Es habitual encontrar una estructura común en la interfaz de resultados, ofreciendo a la izquierda diferentes opciones de filtrado que permiten refinar más los resultados de dicha búsqueda **incluyendo** o **excluyendo** elementos.

Filtros de búsqueda de Scopus
![Filtros de Scopus](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/scopus_filtros.png)

### 2.4. El historial de búsqueda
Tras realizar diferentes pruebas en cualquier momento puedes rescatar alguna de ellas.

### 2.5. Otras búsquedas
#### 2.5.1. Autores
Tanto *Web of Science* como *Scopus* incluyen herramientas de búsqueda específicas para los autores. Estas dan acceso a perfiles de personas que incluyen diferentes métricas, sus publicaciones, etc.

Aunque en ambas herramientas se llevan a cabo tareas de normalización, no evita que existan autores que aparezcan bajo dos o más perfiles diferentes. La opción ideal para localizar personas de forma úniva se encuenta en el uso del **ORCID iD**, pero no todas lo usan/tienen asociado, puede que exista otro perfil.

Al buscar por autor considera las diferentes formas en las que esa persona puede haber firmado.

#### 2.5.2. Referencias citadas
De forma más avanzada y escepífica, en *Web of Science* y *Scopus* está la posibilidad de realizar búsquedas dentro de las referencias bibliográficas de los trabajos indexados.

Gracias a ello es posible recuperar trabajos que citen publicaciones que tengan un autor en concreto, incluyan ciertos términos en el título o estén publicadas en alguna revista en específico, entre otras.


## 3. Herramientas de análisis
Tanto *Web of Science* como *Scopus* incluyen varias herramientas básicas para analizar los registros recuperados en la consulta. Son opciones básicas que resumen de manera visual los datos (publicaciones por año, categoría, principales autores...).

![Gráfico de barras de Web of Science](https://raw.githubusercontent.com/Wences91/teaching/0f79fb3fecdca05ebb7533bd7c497b7372f5a938/images/introducci%C3%B3n_bibliometr%C3%ADa/wos_visualization.jpg)


## 4. Cálculo y análisis de datos automáticos
Gracias a los análisis de citas podemos obtener indicadores bibliométricos básicos en ambas bases de datos. Se trata sin embargo de una opción básica pero que da la posibilidad de realizar un primer acercamiento y a diferentes niveles.

### 4.1. Publicaciones
En el caso de *Web of Science* es posible, analizar las citas de los trabajos recuperados en la búsqueda. Ofrece no solo el total de citas sino la distribución temporal, los valores promedios e índice H. Este es muy similar al disponible en *Scopus*. Podemos ver con ello además cuáles son los documentos que realizan la cita.

Existen sin embargo **límites** en cuanto al números de trabajos en estos análisis.

Distribución anual de citas en Scopus
![Gráfico de citas en Scopus](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/scopus_citations.png)

### 4.2. Autores
A nivel de autor también hay disponible numerosas opciones para el análisis de la producción científica. En ambas herramientas se ofrecen diferentes tipos de visualizaciones y es posible aplicar los anteriores análisis de citas.

Beamplot de citas de Web of Science
![Beamplot de Web of Science](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/beamplot.png)

### 4.3. Instituciones
En ambos casos se pueden llevar a cabo análisis a nivel de institución, aunque *Scopus* incluye opciones de búsqueda, información y análisis especificos para ello.

Datos de la producción de la Universidad de Granada en Scopus
![Beamplot de Web of Science](https://raw.githubusercontent.com/Wences91/teaching/main/images/introducci%C3%B3n_bibliometr%C3%ADa/scopus_ugr.png)


### 4. Suites bibliométricas
De manera más avanzada, existen también **suites bibliométricas** que incluyen muchas más opciones en este sentido e incorporan toda una colección de indicadores. El de Web of Science es InCites y el de Scopus es SciVal.



## Otros recursos
* [Web of Science Help](http://webofscience.help.clarivate.com/en-us/Content/home.htm)
* [Scopus Support Center](https://service.elsevier.com/app/overview/scopus/)

## Referencias
* Alba-Ruiz, R. (2020). Aprender a elaborar ecuaciones de búsqueda bibliográficas. YouTube. https://www.youtube.com/watch?v=m0Rrl2qTUZc
* Arroyo-Machado, Wenceslao. (2021). Cómo no hacer un análisis bibliométrico. Zenodo. https://doi.org/10.5281/zenodo.5624316
* Pranckutė, R. (2021). Web of Science (WoS) and Scopus: The titans of bibliographic information in today’s academic world. Publications, 9(1), 12. https://doi.org/10.3390/publications9010012

---

# Información
<div class="alert alert-block alert-info">
    <b>Autor:</b> Wenceslao Arroyo-Machado</br>
    <b>Fecha de actualización:</b> 24/05/2022</br>
    <b>GitHub:</b> <a href="https://github.com/Wences91/teaching">https://github.com/Wences91/teaching</a>
</div>