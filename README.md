# Spotify Music Analysis before and after coronavirus pandemic

Tras escribir el artículo [¿Es Resistiré una de las canciones más escuchadas en España durante la cuarentena?](https://www.akakicreations.com/es-resistire-una-de-las-canciones-mas-escuchadas-en-espana-durante-la-cuarentena/) y encontrar datos interesantes y sobre todo curiosos, quise indagar en nuestro consumo de música en la pandemia del coronavirus en España. Este proyecto nace de una pregunta sencilla: **¿ha provocado la aparición del coronavirus un cambio en el tipo de música y estilo que se escucha en España?, ¿ha cambiado la música escuchada durante el confinamiento?** Y concretamente me hago cuatro preguntas:
1. ¿Ha provocado un cambio en el tipo de música que se escucha (más bailable, más instrumental, más enérgica...)
2. ¿Ha provocado un cambio en el género de música que se escucha (pop, reggaeton...)?
3. ¿Ha provocado un cambio en si se escuchan más éxitos antiguos?
4.  ¿Qué tipo de música contienen las playlists que se han creado para el tiempo de pandemia?, ¿hay un cambio?

Para esto, nos vamos a basar en datos que nos ofrece Spotify que es la plataforma con [mayor número de usuarios](https://es.statista.com/grafico/19793/usuarios-activos-y-de-pago-de-spotify/) de música en streaming. No es una muestra que pueda ser generalizable, pero si nos puede dar una idea de tendencias y posibles cambios de las mismas.

# Fuentes de datos

 - Fuente de datos que ofrece la [API de Spotify](https://developer.spotify.com/documentation/web-api/) de la que se pueden sacar las características y features de todas las canciones disponibles en Spotify.
   
 - La base de datos de [Spotify Chart](https://spotifycharts.com/regional) donde se pueden extraer las 200 canciones más escuchadas (top200) por día y los respectivos streams (reproducciones) de cada una, ya que este ranking se calcula por el número de veces que se escucha una canción.

# Recomendaciones previas

Este proyecto no requiere instalaciones y entornos concretos aunque se recomienda hacer un git clone y ejecutar en Linux.

Los paquetes que se necesitan para ejecutar correctamente los notebooks son los siguientes:

```!pip install fycharts``` : FychaPara descargar datos del SpotifyChart. Documentación
``` !pip install spotipy``` : Para descargar datos de la API de Spotify. Documentación
 ```!pip install altair vega_datasets```: Para visualización de datos. Documentación
```!pip install seaborn```: Para visualización de datos. Documentación

Se pueden instalar con pip fácilmente
Para poder ejecutar todos los notebooks del proyecto, se recomienda usar el entorno conda que se proporciona en el fichero environment_tfm.yml

Para la creación del entorno ejecutar:


# Análisis y orden de lectura
Hay 4 Notebooks de Jupyter, bien documentados, guiados y explicando todo el proceso. Es recomendable que se lean en el siguiente orden:
1. [Data_ExtractionAndPreparation.ipynb](Data_ExtractionAndPreparation.ipynb): Extracción y preparación de los datasets que luego se usarán en los análisis
2. [Data_Analysis1_Features.ipynb](Data_Analysis1_Features.ipynb): Primer análisis para responder a la primera pregunta: ¿ha habido un cambio en el tipo de música?
3. [Data_Analysis2_Genres.ipynb](Data_Analysis2_genres.ipynb): Segundo análisis para responder a la segunda pregunta: ¿un cambio en el género de música?
4. [Data_Analysis3_Oldies.ipynb](Data_Analysis3_oldies.ipynb): Tercer análisis para responder a la tercera pregunta: ¿un cambio en cantidad de éxitos antiguos escuchados?
5. [Data_Analysis4Extra_Playlists.ipynb](Data_Analysis4Extra_Playlists.ipynb): Cuarto análisis que es una extensión del primero para responder mejor y desde otro dataset a la pregunta: ¿ha habido un cambio en el tipo de música?

# Visualización
En proceso

# Código
Se ha utilizado Python y Jupyter Notebook como herramienta principal y para ciertas visualizaciones Tableau.
Agradecimiento código de terceros:
 - Para la extracción de datos de Spotify Top200Charts: https://github.com/kelvingakuo/fycharts, thanks to [kelvingakuo](https://github.com/kelvingakuo)/
 - Para la extracción de datos de API Spotify: [morioh](https://morioh.com/p/31b8a607b2b0)/ 

# Datasets
En proceso

# Créditos
En proceso
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA2MzM3OTE1MiwxNDQ5NDcxMTc3LDcyNj
M3Mjg5OSw0MjA2NzA5OTcsMTgzMDc1MzUzLC0yMDk0NjAyMDk2
LC0yNjc2OTg2MDYsNTgxMjQ4OTU4XX0=
-->