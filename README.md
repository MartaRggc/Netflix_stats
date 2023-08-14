# Netflix_stats

<p align="center">
  <img src="images/netflix.png" alt="drawing" width="100">
</p>

# Introducción y origen de los datos

En este proyecto he recopilado y limpiado unos datos de uso de la plataforma Netflix, para realizar un posterior análisis gráfico sobre las tendencias de sus usuarios. Mis fuentes han sido tres:

1) Un archivo csv descargado de [kaggle](https://www.kaggle.com/datasets/arnavsmayan/netflix-userbase-dataset), con un dataset sintético (no son datos reales, sino que reflejan tendencias generales de los usuarios de Netflix).
2) Datos scrapeados de [beebom](https://beebom.com/how-much-netflix-costs-each-country-worldwide/), de las tarifas reales de las suscripciones 'premium', 'standard' y 'basic' en los distintos países.
3) Un archivo csv de la página [worldpopulationreview](https://worldpopulationreview.com/country-rankings/purchasing-power-parity-by-country), del que he sacado los datos de Purchasing Power Parity (PPP) para poder comparar el precio relativo de las suscripciones en los distintos países.
   

# 1. Limpieza de datos 

En el jupyter notebook 'Data_extracting_&_cleanning.ipynb' he ido limpiando y agrupando los distintos datos de estas fuentes. He realizado algunos cambios menores sobre la tabla principal de kaggle, como cambiar el formato de las fechas, eliminar columnas redundantes etc., y la he enriquecido con la información de las otras dos fuentes de la siguiente forma:

+ He sustituido la columna de 'revenue' por los precios reales y actualizados de las distintas suscripciones en cada país, expresados en dólares estadounidenses.
+ He añadido el PPP actual de cada país, y he calculado una columna más con un precio relativo de las suscripciones según dicho valor.

Finalmente he guardado el dataframe resultante en un csv, para importarlo después desde PowerBI.

# Análisis



- No hay diferencias significativas en cuanto al uso por género en ningún rango de edad. La mayor parte de los usuarios están entre 30 y 40 años. En cuanto al tipo de suscripción, la más popular es la tarifa básica en que reúne al 40% de los usuarios, frente a los casi igualados 30% de las tarifas premium y standard.
- La mayor parte de las suscripciones más caras 'premium' que hay registradas están en el rango de edad en torno a 30 años. Sin embargo, si agrupamos por género y estudiamos cada subgrupo de edad por separado, vemos que el subgrupo en que hay mayor porcentaje de suscripción premium es el de mujeres en torno a los 25 años.

- Vamos a echar un ojo al porcentaje de usuarios por países.
