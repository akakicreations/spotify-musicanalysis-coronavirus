# Spotify Music Analysis in the coronavirus pandemic

Tras escribir el artículo [¿Es Resistiré una de las canciones más escuchadas en España durante la cuarentena?](https://www.akakicreations.com/es-resistire-una-de-las-canciones-mas-escuchadas-en-espana-durante-la-cuarentena/) y encontrar datos interesantes y sobre todo curiosos, quise indagar en nuestro consumo de música en la pandemia del coronavirus en España. Este proyecto nace de una pregunta sencilla: **¿ha provocado la aparición del coronavirus un cambio en el tipo de música y estilo que se escucha en España?** Y concretamente me hago tres preguntas:
1. ¿Ha provocado un cambio en el tipo de música que se escucha (más bailable, más instrumental, más enérgica...)
2. ¿Ha provocado un cambio en el género de música que se escucha (pop, reggeaton...)?
3. ¿Ha provocado un cambio en si se escuchan más canciones antiguas?

Para esto, nos vamos a basar en datos que nos ofrece Spotify que es la plataforma con [mayor número de usuarios](https://es.statista.com/grafico/19793/usuarios-activos-y-de-pago-de-spotify/) de música en streaming. No es una muestra que pueda ser generalizable, pero si nos puede dar una idea de tendencias y posibles cambios de las mismas.

# Fuentes de datos

 - Fuente de datos que ofrece la [API de Spotify](https://developer.spotify.com/documentation/web-api/) de la que se pueden sacar las características y features de todas las canciones disponibles en Spotify.
   
 - La base de datos de [Spotify Chart](https://spotifycharts.com/regional) donde se pueden extraer las 200 canciones más escuchadas (top200) por día y los respectivos streams (reproducciones) de cada una, ya que este ranking se calcula por el número de veces que se escucha una canción.

# Análisis
Hay 4 Notebooks de Jupyter, bien documentados y que se pueden leer en el siguiente orden para entender el proceso de análisis:
1. Data_ExtractionAndPreparation.ipynb
2. Data_Analysis1_Features.ipynb
3. Data_Analysis2_Genres.ipynb
4. Data_Analysis3_Oldies.ipynb

# Visualización
En proceso

# Código
Se ha utilizado Python como herramienta
Agradecimiento código de otros:
 - Para la extracción de datos de Spotify Top200Charts:
 - En proceso

# Datasets
En proceso

# Crédito
En proceso
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgzMDc1MzUzLC0yMDk0NjAyMDk2LC0yNj
c2OTg2MDYsNTgxMjQ4OTU4XX0=
-->