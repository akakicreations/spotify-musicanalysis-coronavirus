![enter image description here](images_features_distribution/portada_spotify_coronavirus_analysis.png)
# Spotify Music Analysis before and during coronavirus pandemic

Tras escribir el artículo [¿Es Resistiré una de las canciones más escuchadas en España durante la cuarentena?](https://www.akakicreations.com/es-resistire-una-de-las-canciones-mas-escuchadas-en-espana-durante-la-cuarentena/) y encontrar datos interesantes y sobre todo curiosos, quise indagar en nuestro consumo de música durante confinamiento por la pandemia del coronavirus en España, en Marzo de 2020. Este proyecto nace de una pregunta sencilla: **¿provocó la aparición del coronavirus un cambio en el tipo de música que se escuchó en España durante el confinamiento?** Y concretamente me hago cuatro preguntas:
1. ¿Provocó el confinamiento un cambio en el tipo de música que se escuchó (más bailable, más instrumental, más enérgica...)
2. ¿Provocó el confinamiento un cambio en el género de música que se escuchó (pop, dance, reggaeton...)?
3. ¿Provocó el confinamiento un cambio en si se escucharon más éxitos antiguos?
4.  ¿Qué tipo de música contienen las playlists que se han crearon durante el confinamiento?, ¿hay un cambio respecto a otras playslist?

Para esto, nos vamos a basar en datos que nos ofrece Spotify que es la plataforma con [mayor número de usuarios](https://es.statista.com/grafico/19793/usuarios-activos-y-de-pago-de-spotify/) de música en streaming. No es una muestra que pueda ser generalizable, pero si nos puede dar una idea de tendencias y posibles cambios de las mismas.

Los resultados de este estudio están publidos en [esta entrada del blog.](https://www.akakicreations.com/como-afecto-el-confinamiento-por-coronavirus-en-2020-en-el-tipo-de-musica-que-escuchamos-en-spotify-2/)

# Fuentes de datos

 - Fuente de datos que ofrece la [API de Spotify](https://developer.spotify.com/documentation/web-api/) de la que se pueden sacar las características y features de todas las canciones disponibles en Spotify.
   
 - La base de datos de [Spotify Chart](https://spotifycharts.com/regional) donde se pueden extraer las 200 canciones más escuchadas (top200) por día y los respectivos streams (reproducciones) de cada una, ya que este ranking se calcula por el número de veces que se escucha una canción.

# Recomendaciones previas

Este proyecto no requiere instalaciones y entornos concretos aunque se recomienda hacer un git clone y ejecutar todo en Linux.

Los paquetes que se necesitan para ejecutar correctamente los notebooks son los siguientes:

 - **Fycharts:** Para descargar datos del SpotifyChart. [Documentación.](https://pypi.org/project/fycharts/) Instalación: ```!pip install fycharts```
 - **Spotipy:** Para descargar datos de la API de Spotify. [Documentación.](https://spotipy.readthedocs.io/en/2.16.0/) Instalación:``` !pip install spotipy```
 - **Altair:** Para visualización de datos. [Documentación.](https://altair-viz.github.io) Instalación: ```!pip install altair vega_datasets```
 - **Seaborn:** Para visualización de datos. [Documentación.](https://seaborn.pydata.org) Instalación:```!pip install seaborn```:
 -  -**Prophets** Para análisis y predicciones. [Documentación.](https://facebook.github.io/prophet/) Instalación:```!pip install pystan``` , ```!pip install prophet```:

También se ha usado Tableau para la visualización de ciertos análisis y que incluimos también. Aún así, hemos incluido imágenes de los Dashboards dentro de los Notebooks Jupyter.

# Análisis y orden de lectura
Hay 7 Notebooks de Jupyter, los 6 primeros están perfectamente documentados y fueron fruto de un primer análisis, que luego sbien documentados, guiados y explicando todo el proceso. También he dejado en una [carpeta](notebooks_inHTML) los notebooks en formato HTML con todas las celdas ejecutadas por si se quiere ver completo sin usar Jupyter

Los notebooks o HTMLs es recomendable que se lean en el siguiente orden:
1. [Data_ExtractionAndPreparation.ipynb](Data_ExtractionAndPreparation.ipynb): Extracción y preparación de los datasets que luego se usarán en los análisis
2. [Data_Analysis1_Features.ipynb](Data_Analysis1_Features.ipynb): Primer análisis para responder a la primera pregunta: ¿ha habido un cambio en el tipo de música?
3. [Data_Analysis2_Genres.ipynb](Data_Analysis2_genres.ipynb): Segundo análisis para responder a la segunda pregunta: ¿un cambio en el género de música?
4. [Data_Analysis3_Oldies.ipynb](Data_Analysis3_oldies.ipynb): Tercer análisis para responder a la tercera pregunta: ¿un cambio en cantidad de éxitos antiguos escuchados?
5. [Data_Analysis4Extra_Playlists.ipynb](Data_Analysis4Extra_Playlists.ipynb): Cuarto análisis que es una extensión del primero para responder mejor y desde otro dataset a la pregunta: ¿ha habido un cambio en el tipo de música?
6. [Data_Analysis5_MostPlayed.ipynb](Data_Analysis5_MostPlayed.ipynb): Por último, y como datos curiosos, vemos las canciones, artistas y géneros más escuchados durante el confinamiento del coronavirus.
7. [Data_Analysis5_MostPlayed.ipynb](Data_Analysis5_MostPlayed.ipynb): Por último, y como datos curiosos, vemos las canciones, artistas y géneros más escuchados durante el confinamiento del coronavirus.
8. 7.[Data_Analysis5_MostPlayed.ipynb](Data_Analysis5_MostPlayed.ipynb): Por último, y como datos curiosos, vemos las canciones, artistas y géneros más escuchados durante el confinamiento del coronavirus.

Al final de cada Notebook hay unas conclusiones para responder claramente a cada pregunta. 

Próximamente publicaré una presentación y un artículo como resumen de este proyecto.

# Visualizaciones y conclusiones


Para las visualizaciones de datos se han utilizado múltiples herramientas, que se pueden ejecutar desde los propios Notebooks (Pyplot, Seaborn, Altair) y desde fuera (Tableau), que he dejado loa archivos también en la carpeta [tableau_graph_and_analysis](tableau_graph_and_analysis)



# Datasets
En el proceso de extracción análisis se han creado los siguientes datasets de losa ue explico su contenido.

 - Datos de los Top200 de música más escuchada en España de 2017, 2018, 2019 y 2020, desde el 01/01 al 05/20, es un listado de canciones: 
	 - top_200_daily_CSV_2017.csv
	 - top_200_daily_CSV_2018.csv
	 - top_200_daily_CSV_2019.csv
	 - top_200_daily_CSV_2020.csv
- Datos con listado de canciones y sus features añadidas después de la extracción para el Periodo del Confinamiento y para el Periodo Normal, de control, de 2017, 2018, 2019 y 2020:
	- data_global_coronaperiod.csv
	- data_global_normalperiod.csv
- Datos limpios y preparados para análisis:
	- data_ana_coronaperiod.csv
	- data_ana_normalperiod.csv
	- data_ana_coronaperiod_withgenres.csv
- Datos con las canciones de las playlists del 2020 y 2019 en diferentes tamaños de paquetes:
	- data_ana_playlist_songs100.csv
	- data_ana_playlist_songs10000.csv
	- data_ana_playlist_songs100_2019.csv
	
# Código y créditos

Se ha utilizado Python y Jupyter Notebook como herramienta principal y para ciertas visualizaciones Tableau.

Agradezco el código de otras personas y que yo he reutilizado y adaptado, señalo las siguientes:
 - Para la extracción de datos de Spotify Top200Charts: https://github.com/kelvingakuo/fycharts, thanks to [kelvingakuo](https://github.com/kelvingakuo)/
 - Para la extracción de datos de API Spotify: thanks to [morioh](https://morioh.com/p/31b8a607b2b0)
 - Otra mucha documentación sobre extracción de datos de la API de Spotify en internet

# ¡Gracias!

![enter image description here](images_features_distribution/giphy_rock.gif)
<!--stackedit_data:
eyJoaXN0b3J5IjpbODY0ODEzOTQwLDIwODQ2NjY2OSwtMTQ0OT
I5ODI3MCwxNTkyMzg1MTIyLDc0NDYyMTgzMCw2MTk3NDY1OTks
LTY3MzY4NjQ1OSwyMzkxNDU4MTUsODY0NjcxODI4LDkxMTM4Nz
kyNiwtMTUwMTAyMzksNjMyODIxOTUwLDUxNTcxMDc4OCwtNDk0
NDkxMDQ5LDE0NDk0NzExNzcsNzI2MzcyODk5LDQyMDY3MDk5Ny
wxODMwNzUzNTMsLTIwOTQ2MDIwOTYsLTI2NzY5ODYwNl19
-->