# Introducción a las principales bases de datos bibliométricas (Web of Science y Scopus)

## 1. Lenguaje de consulta
Es crucial en un análisis bibliométrico realizar una correcta búsqueda. Pese a las facilidades que ofrecen muchas de las interfaces de búsqueda de las bases de datos bibliográficas, este proceso requiere especial atención. Una incorrecta búsqueda puede conducir a datos con mucho ruido, poco o demasiado exhaustivos...

### 1.1. El proceso de búsqueda
De manera general el proceso de búsqueda plantea los siguientes pasos:
1. **¿Qué quieres buscar?** - Elaboración de una pregunta
2. **¿Dónde vas a buscar?** - Selección de una base de datos (cobertura, sesgo, especialización...)
3. **Consulta** - Elaboración de la búsqueda
4. **Depura la consulta** - Ajuste y repetición de la consulta

Resueltos los dos primeros pasos llega el turno de la consulta en la base de datos. Esta precisa de una correcta estrategia y por lo general requiere de varios intentos, pruebas y comprobaciones antes de dar con la más adecuada. **Nunca te conformes a la primera**.

No va a ser lo habitual que nuestra **ecuación de consulta** esté conformada de un único término o campo de búsqueda, suelen intervenir diferentes elementos. Para elaborar dicha consulta existe todo un lenguaje en el que se suele encontrar:
* **Operadores booleanos** - Común a casi todos los buscadores y que es crucial dominar.
* **Otros operadores comunes** - Junto a los booleanos, la mayoría suelen permitir su uso.
* **Operadores de campo** - Permiten indicar el campo exacto en el que se busca un término. Aunque pueden existir elementos comunes, cada buscador cuenta con campos especificos.

### 1.2. Operadores booleanos
Estos operadores están basados en el álgebra de Boole y permite hacer búsqueda precisas indicando en nuestra ecuación de consulta cómo han de combinarse dos o más elementos de la consulta:

Los operadores básicos son tres:
* **OR** - booleano de unión. Devuelve registros que cumplan uno o ambos criterios. Búsquedas poco restrictivas.
* **AND** - booleano de intersección. Devuelve solo los registros que cumplen ambos criterios. Búsquedas restrictivas.
* **NOT** - booleano de exclusión. Devuelve los registros que cumplen el primer critero pero no el segundo. Búsquedas restrictivas.

Pero cuidado, aunque se usen en prácticamente casi todos los buscadores, puede haya variaciones en su denominación. Por ejemplo, **NOT** puede aparecer así o como **-**.

### 1.3. Otros operadores comunes
En línea con los los operadores booleanos existen otros que también suelen ser comunes en los buscadores y que resultan imprescindibles. De manera general se puede destacar:
* **()** - los paréntesis hacen posible agrupar operadores cuando la ecuación de consulta involucra más de uno.

Por otro lado, al introducir términos de busqueda, podemos manipular dichas cadenas para hacerlas más o menos restrictivas con:
* **""** - las comillas permiten buscar cadenas de texto exactas.
* **\*** - gracias al asterisco se puede llevar a cabo el truncamiento de uno o varios caracteres.


## 2. Búsquedas bibliográficas
### 2.1. Primeros pasos
La mayoría de bases de datos bibliográficas disponen de dos tipos de búsquedas:
* **Busqueda simple**
* **Busqueda avanzada**

Por defecto, veremos en la mayoría de ocasiones la búsqueda simple al entrar en las bases de datos bibliográficas. Esta es una busqueda más guiada en el que la interfaz nos facilita la consulta mediante elementos visuales, por ejemplo con diferentes cajas de búsqueda para cada campo de búsqueda y la posibilidad de indicar el operador booleano que los conecta. La búsqueda avanzada consiste en una única caja de consulta en la que se introduce la ecuación de consulta completa incluyendo tanto los campos y términos como los operadorer.

En el caso de *Web of Science*, se pueden filtrar las bases de datos que se usan en la búsqueda. Presta atención a ello, porque los campos de búsqueda o filtros pueden variar. Por lo general usa la **Web of Science Core Collection**, dentro de la cual puedes seleccionar varias bases de datos en específico, siendo las principales:
* Science Citation Index Expanded (SCI)
* Social Sciences Citation Index (SSCI)
* Arts & Humanities Citation Index (AHCI)
* Emerging Sources Citation Index (ESCI)

### 2.2. Aspectos a tener cuenta
Más allá del tipo de búsqueda, hay dis aspectos que siempren han de considerarse en cualquier búsqueda bibliográfica:
- [x] **Fecha de publicación** - Por norma general, considera solo los años completos y ten en cuenta que análisis quieres realizar para centrar la atención en un periodo más o menos extenso y/o reciente.
- [x] **Tipología documental** - En función del análisis emplea solo aquellas tipologías realmente relevantes.

A la hora de fijar la **temática** no despistes el uso de **categorías** de la base de datos (Research/Subject Categories en Web of Science, Subject Areas en Scopus). Estas son las que indican que una publicación pertenece a un disciplina concreta. Su uso con la búsqueda de términos (título, abstract y palabras clave) puede generar confusión.

Por ejemplo, para buscar publicaciones de Wikipedia relativas a las Ciencias Sociales tenemos dos opciones:
1. ~~**Palabras clave**: Wikipedia AND "Ciencias Sociales"~~
2. **Palabras clave**: Wikipedia AND **Área**:"Ciencias Sociales"

Con independencia de la búsqueda efectuada, los resultados serán mostrados en una página que nos permite filtrar más los resultados.

### 2.3. El filtrado
Es también habitual encontrar una estructura común en la interfaz de resultados, ofreciendo a la izquierda diferentes opciones de filtrado que permiten concretar más los resultados de dicha búsqueda.

### 2.4. El historial de búsqueda

### 2.5. Otras búsquedas
#### 2.5.1. Autores
Tanto *Web of Science* como *Scopus* incluyen herramientas de búsqueda específicas para los autores.

#### 2.5.2. Referencias citadas
De forma más avanzada y escepífica, en *Web of Science* está la posibilidad de realizar búsquedas dentro de las referencias bibliográficas de los trabajos indexados.


## 3. Herramientas de análisis
Tanto *Web of Science* como *Scopus* incluyen varias herramientas básicas para analizar los registros recuperados en la consulta. Son opciones básicas que resumen de manera visual los datos (publicaciones por año, categoría, principales autores...).

![Gráfico de barras de Web of Science](https://raw.githubusercontent.com/Wences91/teaching/0f79fb3fecdca05ebb7533bd7c497b7372f5a938/images/introducci%C3%B3n_bibliometr%C3%ADa/wos_visualization.jpg)


## 4. Cálculo y análisis de datos automáticos
En el caso de *Web of Science* es posible, analizar las citas de los trabajos recuperados en la búsqueda.


De manera más avanzada, existen también **suites bibliométricas** que incluyen muchas más opciones en este sentido e incorporan toda una colección de indicadores. El de Web of Science es InCites y el de Scopus es SciVal.



## Otros recursos
* Arroyo-Machado, Wenceslao. (2021). Cómo no hacer un análisis bibliométrico. Zenodo. https://doi.org/10.5281/zenodo.5624316
