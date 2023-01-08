
# Proyecto Yelp: Predicción de la opinión de los usuarios de restaurantes basado en Análisis de Sentimiento de las revisiones y características del negocio.

## Machine Learnig

### Objetivos y soluciones.
* **Procesar un volumen de información elevado**: Se cargan los grandes ficheros en formato json. Se transforman todas las caracterisiticas de las tablas business, reviews a tablas tidy, Se opta por el formato parquet para las tablas obtenidas.  Cuando es necesario se hace lectura a trozos ( chunks), fusionando cada uno de los chunks con otra tabla que hace de filtro.
Se recurre a trabajar en Colab, para disponer de máquinas de 27  gigas de Ram.
 
 * **Visualizaciones geoespaciales** : Se utiliza para entender la distribución de los negocios y se facilita herramienta para poder observar la escala temporal y geoespacial de las revisiones de un usuario.
 *  **Grafos** : Se genera una red  10.000 usuarios de restaurantes de Santa Barbara, descubriendo las comunidades que los forman.
 * **Analisis de sentimiento**: Se utiliza **VADER** para calificar el sentiento de las revisiones de los usuarios de restaurantes. 
 * Para cada negocio utilizaremos la media del compound de sus revisiones. 
 * **Presentación de los negocios**: Se genera una característica cuantificando la especificidad o especialización de las categorías de como se presentan los restaurantes al público en Yelp. 

Basandonos en el análisis de sentimiento y otras caracterisiticas, se construye un modelo de calificación para predecir la opinión de los clientes en tres categorias en la escala de estrellas, ( Negativa, neutra, positiva), 
Se intenta aproximación con Naive Bayes, Random Forrest y Xgboost. Realizando optimización de hiperparametros para los dos últimos.

Se alcanzan porcentajes de acierto, en términos de accuracy y F-1 superiores al 80 %. Siendo el análisis de sentimiento, el número de revisiones y la especificidad de las categorías con las que el restaurante se presenta al cliente, los factores que mas contrbibyen a discirminar la clase en la que se predice la categoria de los restaurantes.

Autor: Pablo Soto López
Correo: Sotopablolopez@gmail.com 
Ruta proyecto: https://github.com/PabloSotoLopez/Yelp_project.git
