# Aprende a descargar datos de Twitter sin programar

---

# 1. La API de Twitter
El principal punto de acceso para la recuperación y descarga de datos de Twitter es su API. Como ocurre con otras APIs su uso requiere de conocimientos básicos de programación para poder exprimilar completamente. Existen paquetes que simplifican su uso como [academictwitteR](https://cran.r-project.org/web/packages/academictwitteR/) en R, pero es posible que incluso con ello no resulte accesible.

Actualmente la **Twitter API v2** ofrece diferente herramientas adicionales que facilitan y simplifican su uso, entre ellos **Tweet Downloader**, una interfaz visual desde la cual es posible realizar consultas y descargas de datos en la API de Twitter. Su uso es sencillo y ofrece diferentes campos y operadores de búsqueda con los que construir consultas a medida y recuperar datos que son facilmente importables en otras herramientas para su análisis.

# 2. Accediendo a la API de Twitter
En cualquier caso, para poder hacer uso de la API es necesario solicitar acceso. Existen [tres planes de acceso](https://developer.twitter.com/en/docs/twitter-api/getting-started/about-twitter-api):
+ Essential
+ Elevated
+ [Academic Research](https://developer.twitter.com/en/products/twitter-api/academic-research)

El punto de partida es Essential. La [solicitud es sencilla](https://developer.twitter.com/en/docs/twitter-api/getting-started/getting-access-to-the-twitter-api), se basa en un pequeño formulario, y tras ello puedes solicitar expandir tu cuenta a un plan superior. Si eres estudiante de doctorado/máster, la opción Academic Research es perfecta y, además, **obligatoria** para usar **Tweet Downloader**. En este caso es necesario ofrecer más detalles acerca de tu investigación y el uso que le vas a dar a la API.

**A tener en cuenta:** En los tres casos existen limitaciones especificas, a destacar el número de tuit a descargar mensualmente. Puedes comprobar tu uso desde tu [dashboard](https://developer.twitter.com/en/portal/dashboard).

## 2.1. Claves de acceso
Una vez te hayan concedido acceso a la API tendrás un proyecto en tu espacio en el portal de desarrollador. Dentro de este puedes crear una app y a través de ella hacer uso de la API. Las apps ofrecen diferentes claves que son las que permiten la autentificación para hacer uso de la API. Existen varias:

+ **API Key** - Puede verse como el nombre de usuario
+ **API Key Secret** - Puede verse como la contraseña
+ **Bearer Token** - Clave única que simplifica la autentificación en procesos de descarga (necesaria para Tweet Downloader)

**A tener en cuenta:** Cada vez que ejecutes una consulta aparecerá el número de tuits que se ajustan a ella. Hasta que no los descargues no se sumaran a tu contador. De igual manera, antes de bajar grandes volúmenes de datos prueba con una pequeña muestra para comprobar la estructura de datos.


# 3. Uso de Tweet Downloader
[Tweet Downloader](https://developer.twitter.com/apitools/downloader) ofrece la posibilidad de llevar a cabo varias descargas de tuits de manera simultanea. También se encarga de parar las descargas cuando hay errores de conexión y retomarlas una vez se soluciona.

**A tener en cuenta:** En este momento solo puede accederse desde  Chrome, Edge u Opera.

## 3.1. Construcción de una consulta
Las consultas pueden establecerse de manera **avanzada** escribiendo manualmente la ecuación de consulta o de forma **simple** usando las diferentes opciones de la interfaz. En este último caso, se pueden aplicar diferentes filtros y combinarlos mediante los operadores booleanos básicos (AND, OR y NOT).

Es posible hacer busquedas filtrando por información más allá del contenido del tuit como su autoria, localización o idioma, entre otros.


## 3.2. Campos a descargar
Una vez la consulta esté lista, se pueden especificar los metadatos a descargar del tuit, los cuales pueden incluir información de otras entidades más allá del propio tuit:
+ Contenido multimedia (media)
+ Encuesta (poll)
+ Usuario (user)
+ Localización (place)

En caso de querer recuperar datos de alguna de estas entidades es necesario usar expandirlas mendiate **expansions**. Por ejemplo, para descargar datos relativos al lugar en el que se publicó el tuit, no todos lo incluyen, hay que expandir la consulta a *geo.placeid* y seleccionar los diferentes campos de la localización (*place.fields*), como el nombre del lugar (*name*), del país (*country*) o información geográfica (*geo*), que incluye las coordenadas del lugar.

**A tener en cuenta:** Indicar que descargue un metadato especifico, como la localización, no significa que solo se recuperen todos aquellos tuits que lo incluyen.

Los dos formatos de descarga disponibles son: csv y json. No obstante, el formato csv a veces puede incluir campos anidados como en un JSON.


---

# Información
<div class="alert alert-block alert-info">
    <b>Autor:</b> Wenceslao Arroyo-Machado</br>
    <b>Fecha de actualización:</b> 24/06/2022</br>
    <b>GitHub:</b> <a href="https://github.com/Wences91/teaching">https://github.com/Wences91/teaching</a>
</div>