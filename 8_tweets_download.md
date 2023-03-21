# Taller 2. Recuperación de tuits ~~con Tweet Downloader~~ y análisis de datos
Nota: inicialmente este curso iba a estar centrado en [Tweet Downloader](https://developer.twitter.com/apitools/downloader). Pero vivimos en tiempos convulsos y desde [enero](https://twittercommunity.com/t/tweet-downloader-did-not-work/183125) no hay rastro de tal aplicación y no se la espera. La solución a este problema, lejos de rendirnos 😔, es explorar las diferentes alternativas para todos los niveles 👨‍👩‍👧.

<center><img src="https://raw.githubusercontent.com/Wences91/teaching/main/images/tweet_downloader/tweet_downloader_error.JPG"></img></center>

# Objetivos de esta sesión
* Introducir los fundamentos en el acceso a las APIs y web scraping
* Aprender a solicitar acceso a la API de Twitter
* Conocer los aspectos claves para la consulta de Twitter
* Explorar las diferentes opciones para la recuperación de tuits

# 1. Acceso a los datos
## 1.1. API
El Santo Grial 🏆 para el acceso a los datos de Twitter es la API (*Application Programming Interface*). Antes de seguir explorando el potencial de esta API comentar un poco qué es eso de una API 🤷‍♀️.

### Pequeña explicación
Una API es un [intermediario que permite que una aplicación se comunique con otras](https://es.wikipedia.org/wiki/API), en nuestro caso, para solicitar datos. Las APIs se han convertido en el nuevo estándar en el acceso y recuperación de información 👩‍💻, permitiendo hacer recuperación de datos a medida.

Existen diferentes arquitecturas, pero una de las más comunes es la REST (**RE**presentational **S**tate **T**ransfer). Esta puede verse de igual manera que el acceso a una página web:
1. Desde un cliente (navegador) se accede a una URL 🔗 - en el caso de las API tienen dos partes fundamentales (endpoint y parámetros)
2. La petición se resuelve ✅ - la API gestiona la petición y devuelve un archivo como resultado (en las APIs el estándar es el JSON)

Como ejemplo de funcionamiento de una API, esta sería una petición de búsqueda de publicaciones científicas que tengan en el título la palabra Twitter 🐦 a la base de datos OpenAlex:

https://api.openalex.org/works?filter=title.search:twitter

Este es otro ejemplo, en este caso buscando en la Wikipedia española páginas que tengan de título la palabra Twitter 🐦:
https://es.wikipedia.org/w/api.php?action=opensearch&search=Twitter

❗ **Importante**: No todas las APIs permiten buscar libremente.

### La API de Twitter
Actualmente, también como un cambio [muy reciente](https://twitter.com/TwitterDev/status/1621026986784337922), Twitter solo ofrece acceso a sus datos mediante la Twitter API V2.

Como decíamos, no todas las APIs se pueden consultar de manera abierta 😢. Twitter requiere de ciertos permisos para consultar su API. Existen diferentes [niveles de acceso](https://developer.twitter.com/en/docs/twitter-api) ahora mismo, los cuales son altamente probable que se vean alterados muy pronto, incluso con [nuevos modelos gratuitos](https://twitter.com/TwitterDev/status/1629865830337990656):
* Essential
* Elevated
* Elevated+
* Academic Research 💙 ([actualmente en revisión](https://developer.twitter.com/en/products/twitter-api/academic-research/application-info))

### Academic Research
Para solicitar acceso al modelo Academic Research es necesario en primer lugar solicitar el [acceso básico](https://developer.twitter.com/en/portal/petition/essential/basic-info) (Essential) y tras ello solicitarlo. Son varias las [recomendaciones a tener en cuenta](https://twarc-project.readthedocs.io/en/latest/twitter-developer-access/).

⚠️ **Advertencia**: desde enero [no parece](https://twittercommunity.com/c/academic-research/62) que las peticiones se estén resolviendo.

Una vez tengas acceso 🍀 tendrás un proyecto de acuerdo a la solicitud y podrás crear aplicaciones con las que consultar la API de Twitter.

### Search tweets
Para la [búsqueda de tweets](https://developer.twitter.com/en/docs/twitter-api/tweets/search/introduction) hay dos endpoints:
* [**Recent search**](https://developer.twitter.com/en/docs/twitter-api/tweets/search/quick-start/recent-search) - Tuits recientes (últimos 7 días)
* [**Full-archive search**](https://developer.twitter.com/en/docs/twitter-api/tweets/search/quick-start/full-archive-search) - Todos los tuits

Para acceder al *Full-archive search* endpoint necesitas la cuenta académica 😔.

## 1.2. Web scraping
Esta es una alternativa a la API muy popular. El web scpraing es la técnica mediante la cual se replica el comportamiento humano en la web para realizar una [extracción automatizada](https://es.wikipedia.org/wiki/Web_scraping) ⚙️ de datos.

En el caso de Twitter, esta práctica significa crear aplicaciones que ejecuten búsquedas de tuits y se vayan desplazando por el *timeline* para recuperar todos los tuits que ahí aparecen 🐀.

No faltan incluso [aplicaciones](https://www.graphext.com/docs/scraping-with-tractor) que incorporan técnicas de scraping para obtener datos de medios sociales.

❗ **Importante**: De igual manera, son varias las recomendaciones desde los puntos de vista [éticos 🦌, legales ⚖️ y metodológicos 🧫](https://eprints.whiterose.ac.uk/126729/).

# 2. Construcción de una consutla
Con independencia a la forma de acceso a los datos de Twitter el punto clave está siempre en la elaboración de un correcta consulta. Más aún si el acceso a los datos está limitado y un fallo puede hacerte perder bastante tiempo de espera.

Existe toda una [sintaxis](https://developer.twitter.com/en/docs/twitter-api/tweets/search/integrate/build-a-query) repleta de posibilidades para elaborar consultas, pero los elementos que con seguridad más vas a necesitar son:
* [**Operadores booleanos**](https://developer.twitter.com/en/docs/twitter-api/tweets/search/integrate/build-a-query#boolean) - Indican como se combinan los términos y operadores de campo
  * OR (por defecto)
  * AND
  * NOT (-)
* [Operadores de campo](https://developer.twitter.com/en/docs/twitter-api/tweets/search/integrate/build-a-query#list) - Permiten filtrar de manera precisa (p. ej.; los tuits publicados por una cuenta concreta o en una fecha determinada)

🌮 **Consejo**: Haz uso de la [búsqueda avanzada](https://twitter.com/search-advanced?vertical=trends) para construir un consulta a completa medida.

Al final de este proceso necesitas tener la consulta exacta, por ejemplo:

```
coronavirus since:2020-01-01 until:2020-02-28
```

### Ejemplos

Una vez vistos los operadores básicos, veámos varios ejemplos básicos:
<details> 
  <summary><b>Ejemplo 1</b> - Tuits publicados por la cuenta de @el_pais que hagan mención a chatGPT</summary>
  <b>Consulta</b>: chatgpt from:el_pais
</details>
<details> 
  <summary><b>Ejemplo 2</b> - Tuits en español con el hashtag #Mandalorian en el día de su estreno (12 de noviembre de 2019)</summary>
  <b>Consulta</b>: #Mandalorian lang:es since:2019-11-12 until:2019-11-13
</details>
<details> 
  <summary><b>Ejemplo 3</b> - Tuits sobre la Ley Trans el 1 y 2 de marzo pero que no hagan mención a la propuesta de derogación</summary>
  <b>Consulta</b>: (leytrans OR "ley trans") -derogacion -derogar -eliminar -eliminara since:2023-03-01 until:2023-03-03
</details><br>

🌮 **Consejo**: Antes de lanzar cualquier búsqueda, asegúrate desde la web de Twitter que los resultados que ofrece son exactamente los que quieres y que no faltan o sobran términos relevantes.

# 3. Herramientas para recuperar tuits
Son mcuchas las alternativas para la recuperación de tuits.

| Aplicación                                | Descripción                                                             | API | Programación | Datos                |
|-------------------------------------------|-------------------------------------------------------------------------|-----|--------------|----------------------|
| [**Twitter API V2**](https://developer.twitter.com/en/docs/twitter-api)                        | API de Twitter                                                          | ✔️   | ✔️            | Todos                |
| [**academictwitteR**](https://github.com/cjbarrie/academictwitteR)                       | Paquete de R para la consulta de la API de Twitter                      | ✔️   | ✔️            | Cuentas y tuits      |
| [**Postman**](https://developer.twitter.com/en/docs/tutorials/postman-getting-started)                               | Interfaz para la consulta de APIs                                       | ✔️   | ❌            | Todos                |
| [**Twitter Streaming Importer V2 (Gephi)**](https://gephi.org/plugins/#/plugin/twitter-v2) | Plugin de Gephi para el seguimiento de actividad en directo de Twitter  | ✔️   | ❌            | Actividad en directo |
| [**Web Scraper**](https://webscraper.io/)                           | Plugin de navegador para scraping                                       | ❌   | ❌            | Tuits                |
| [**Twitter Scraper**](https://chrome.google.com/webstore/detail/twitter-scraper/cedomiiokkcmbeoekchahgmfcppnclal)                       | Plugin de navegador para el scraping de los tuits de usuarios concretos | ❌   | ❌            | Tuits                |

Twitter también [lista diferentes herramientas](https://developer.twitter.com/en/docs/twitter-api/tools-and-libraries/v2) para acceder a sus datos. Incluso de manera específica para la [búsqueda de tuits](https://developer.twitter.com/en/docs/twitter-api/tweets/search/introduction).

## 3.1. Twitter API
Este es el proceso básico y más avanzado. Aquí necesitas construir la URL de manera manual, revisando la opción de [*full-archive search*](https://developer.twitter.com/en/docs/twitter-api/tweets/search/quick-start/full-archive-search) y el tipo de objeto [*tweet*](https://developer.twitter.com/en/docs/twitter-api/data-dictionary/object-model/tweet).

Lo que hacemos mediante programación es básicamente automatizar este acceso y procesamiento de respuestas 🏎️.

## 3.2. academictwitteR
En primer lugar tienes que instalar el paquete.

```
install.packages('academictwitteR')
```

Tras ello el funcionamiento es muy sencillo. Solo con usar la función ```get_all_tweets()``` puedes recuperar los tuits indicando unos parámetros básicos:
* **query** - consulta
* **start_tweets** - fecha de inicio (p. ej.: 2023-03-19T00:00:00Z)
* **end_tweets** - fecha final (p. ej.: 2023-03-21T00:00:00Z)
* **bearer_token** - token
* **n** - tuits máximos

## 3.3. Postman
El primer paso es registrarse, puedes directamente registrate desde una cuenta de gmail ✉️.

Tras ello, Twitter ofrece todo un [entorno](https://t.co/twitter-api-postman) preparado para consultar su API, cópialo (*fork*) a tu colección y ve a Search Tweets/Full-archive search.

Necesitas realizar los siguientes pasos:
1. Introducir tu *bearer token* en autorización
2. Introducir el parámetro *query*
3. Introducir los parámetros field y/o expansion (opcional)
4. Introducir el parámetro max_results (opcional)

❗ **Importante**: Solo puedes buscar en cada consulta un máximo de 100 tuits (por defecto son 10). Si excedes los límites, la consulta te indicará al final un *next_token* ⏭️ el cual tendrás que incluir como un campo más para continuar a partir de aquí en una siguiente consulta.

## 3.4. Twitter Streaming Importer V2 (Gephi)
Este es muy sencillo pero los datos que recuperan son diferentes. Esta herramienta permite hacer una escucha de Twitter en directo 📣, no permite recuperar tuits que ya hayan sido publicados previamente sino que hace un seguimiento de todo lo que se va publicando desde que lo inices.

Por ejemplo, vamos a ver qué se está publicando en Twitter con el hashtag
#DíaInternacionaldelosBosques.

## 3.5. Web Scraper
Este es una de las muchas herramientas que permiten hacer web scraping 🕷️. Su funcionamiento básico es muy sencillo:
1. Estableces una consulta en Twitter y obtienes la URL de la consulta en la que vienen los tuits que quieres recuperar
2. Se establece un protocolo de búsqueda para que se desplace por la página hasta alcanzar el final
3. Se establecen los metadatos exactos a recuperar de cada tuit

## 3.6. Twitter Scraper
Esta aplicación es específica de Google Chrome y simplifica el proceso, permitiendo hacer scraping de los tuits de usuarios concretos.
