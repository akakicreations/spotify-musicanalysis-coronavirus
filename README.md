![enter image description here](images_features_distribution/portada_spotify_coronavirus_analysis.png)
# Spotify Music Analysis before and during coronavirus pandemic

Tras escribir el artículo [¿Es Resistiré una de las canciones más escuchadas en España durante la cuarentena?](https://www.akakicreations.com/es-resistire-una-de-las-canciones-mas-escuchadas-en-espana-durante-la-cuarentena/) y encontrar datos interesantes y sobre todo curiosos, quise indagar en nuestro consumo de música durante confinamiento por la pandemia del coronavirus en España, en Marzo de 2020. Este proyecto nace de una pregunta sencilla: **¿provocó la aparición del coronavirus un cambio en el tipo de música que se escuchó en España durante el confinamiento?** Y concretamente me hago cuatro preguntas:
1. ¿Provocó el confinamiento un cambio en el tipo de música que se escuchó (más bailable, más instrumental, más enérgica...)
2. ¿Provocó el confinamiento un cambio en el género de música que se escuchó (pop, dance, reggaeton...)?
3. ¿Provocó el confinamiento un cambio en si se escucharon más éxitos antiguos?

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

# Análisis y orden de lectura
Hay 7 Notebooks de Jupyter, los 6 primeros están perfectamente documentados y fueron fruto de un primer análisis. También he dejado en una [carpeta](notebooks_inHTML) los notebooks en formato HTML con todas las celdas ejecutadas por si se quiere ver completo sin usar Jupyter. Estos 6 notebooks utilizan los datos que están en la carpeta "data_coronaperiods_years2017-2020" que sólo recogen datos de piropos concretos del año. 

Los notebooks o HTMLs es recomendable que se lean en el siguiente orden:
1. [Data_ExtractionAndPreparation.ipynb](Data_ExtractionAndPreparation.ipynb): Extracción y preparación de los datasets que luego se usarán en los análisis
2. [Data_Analysis1_Features.ipynb](Data_Analysis1_Features.ipynb): Primer análisis para responder a la primera pregunta: ¿ha habido un cambio en el tipo de música?
3. [Data_Analysis2_Genres.ipynb](Data_Analysis2_genres.ipynb): Segundo análisis para responder a la segunda pregunta: ¿un cambio en el género de música?
4. [Data_Analysis3_Oldies.ipynb](Data_Analysis3_oldies.ipynb): Tercer análisis para responder a la tercera pregunta: ¿un cambio en cantidad de éxitos antiguos escuchados?
5. [Data_Analysis4Extra_Playlists.ipynb](Data_Analysis4Extra_Playlists.ipynb): Cuarto análisis que es una extensión del primero para responder mejor y desde otro dataset a la pregunta: ¿ha habido un cambio en el tipo de música?
6. [Data_Analysis5_MostPlayed.ipynb](Data_Analysis5_MostPlayed.ipynb): Por último, y como datos curiosos, vemos las canciones, artistas y géneros más escuchados durante el confinamiento del coronavirus.

Los dos últimos son de un análisis posterior desde otra perspectiva y usando la predicción y datos de la carpeta "data_all_years2017-2020" que analiza datos de los años completos.

7. [Data_Analysis6_FINAL_PROPHETS_ExtractionAndPreparation.ipynb](7.Data_Analysis6_FINAL_PROPHETS_ExtractionAndPreparation.ipynb): Extracción y preparación de los datasets que luego se usarán en el análisis productivo.
8. [Data_Analysis6_Features_FINAL_PROPHETS_YEAR.ipynb](8.Data_Analysis6_Features_FINAL_PROPHETS_YEAR.ipynb): Hacemos el mismo análisis pero comparando los datos del 2020 con una predicción hecha con Prophets

# Visualizaciones

Para las visualizaciones de datos se han utilizado múltiples herramientas, que se pueden ejecutar desde los propios Notebooks (Pyplot, Seaborn, Altair) y desde fuera (Tableau).

Aquí dejo algunos gráficos de las conclusiones finales, pero se puede ver todo en [esta entrada del blog.](https://www.akakicreations.com/como-afecto-el-confinamiento-por-coronavirus-en-2020-en-el-tipo-de-musica-que-escuchamos-en-spotify-2/) Los gráficos en el blog están creados con Datawrapper.

![enter image description here](images_features_distribution/danceability1.png)

![enter image description here](images_features_distribution/danceability2.png)

![enter image description here](images_features_distribution/genres.png)

![enter image description here](images_features_distribution/oldies.png)

# Conclusiones

 - **¿Provocó el confinamiento un cambio en el tipo de música que se escuchó (más bailable, más instrumental, más enérgica...)**
Durante el confinamiento hemos escuchado más música…
Más enérgica, es decir, con más velocidad, sonoridad y ruido respecto de la predicción.
Más en directo o con público detrás respecto de la predicción.
Más acústica, es decir con menos acumulación de sonidos e instrumentos y una predominancia importante de la voz.
Más popular y de éxitos que se escuchan muchísimas veces, es decir, menor variedad musical.
Menos bailable, es decir, con menor tempo, ritmo y fuerza de los «beats».
Menos positiva, de felicidad, eufórica, música con la que dan ganas de saltar de alegría.

 - **¿Provocó el confinamiento un cambio en el género de música que se escuchó (pop, dance, reggaeton...)?**
No se puede decir que la pandemia haya provocado un cambio relevante en el tipo de género de música que se escuchaba, está ligado a otros factores.

 - **¿Provocó el confinamiento un cambio en si se escucharon más éxitos
   antiguos?**
   Sí, en el confinamiento se escuchó más música antigua.

# Datasets
En el proceso de extracción análisis se han creado los siguientes datasets de lo que explico su contenido.

DATOS DE LA CARPETA  [data_coronaperiods_years2017-2020](data_coronaperiods_years2017-2020):
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
	
DATOS DE LA CARPETA  [data_all_years2017-2020](data_all_years2017-2020):
- En esta carpeta hay un archivo comprimido "data_ana_timeseries_final.csv.zip" donde se recogen todos losdatos de los años 2017-2020 del Top200 en España.

# Código y créditos

Se ha utilizado Python y Jupyter Notebook como herramienta principal y para ciertas visualizaciones Tableau.

Agradezco el código de otras personas y que yo he reutilizado y adaptado, señalo las siguientes:
 - Para la extracción de datos de Spotify Top200Charts: https://github.com/kelvingakuo/fycharts, thanks to [kelvingakuo](https://github.com/kelvingakuo)/
 - Para la extracción de datos de API Spotify: thanks to [morioh](https://morioh.com/p/31b8a607b2b0)
 - Otra mucha documentación sobre extracción de datos de la API de Spotify en internet

# ¡Gracias!

![enter image description here](images_features_distribution/giphy_rock.gif)
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTgxNzc1MDUwLDEzMzE4ODI5MDEsMzM1Nj
E1ODQ2LC0xOTc2Mzg1MTcwLC0xMjkyMzI0Nzk4LC0xODg0NTQ4
OTM5LDIwODQ2NjY2OSwtMTQ0OTI5ODI3MCwxNTkyMzg1MTIyLD
c0NDYyMTgzMCw2MTk3NDY1OTksLTY3MzY4NjQ1OSwyMzkxNDU4
MTUsODY0NjcxODI4LDkxMTM4NzkyNiwtMTUwMTAyMzksNjMyOD
IxOTUwLDUxNTcxMDc4OCwtNDk0NDkxMDQ5LDE0NDk0NzExNzdd
fQ==
-->