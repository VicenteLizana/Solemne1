# Selección de datos
Seleccionamos los datos de acceso en un tiempo determinado desde ciertas zonas a centros vacunatorios para covid-19 en Estados Unidos y Puerto Rico, disponibles en Google Cloud. Esto nos dará una percepción para comparar la conectividad que presentan distintos estados y generar hipotesis acerca de las preferencias de sus planificaciones urbanas, ya que se presentan distintos medios para acercarse.

Los datos se obtuvieron de: https://console.cloud.google.com/marketplace/product/bigquery-public-datasets/covid19-vaccination-access, que representa lo medido en Estados Unidos entre junio de 2021 y septiembre de 2022.


## Datos
Los datos estan separados por una tabla para cada medio de transporte y una tabla que acumula todos. Se carga la tabla que contiene los datos de todos y se utiliza BigQuery para poder visualizarlos:

![Datos brutos](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Datos%20brutos.png)

De esta forma se pueden eliminar las columnas de datos que son redundantes, en este caso, las columnas que se presentarían despues de limpiar son: nombre de la instalación, pais, estado/subregión, medio de transporte y tiempo de viaje.
Esto reduce la tabla de 15 a 5 columnas, haciendo que sea mas facil gestionar la información.

Se realiza un query que cumpla los requisitos mencionados y obtenemos una tabla mas manejable:

![Datos limpios](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Datos%20limpios.png)

Podemos realizar una mejor observación contando las veces que se repiten nombres o valores por cada columna:

![Conteo de datos](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Conteo%20de%20datos.png)

Vemos ciertos nombres que se repiten bastante(En el código están los datos totalmente desplegados), por ejemplo, en los nombres de la instalación se repiten mucho los nombres CVS Pharmacy, Walgreens Pharmacy, Walmart y Rite Aid. Si observamos el conteo de paises podemos darnos cuenta de algo interesante:

![]()

Estados Unidos corresponde a un 99,62% de los datos totales, por lo que podemos tomar toda la data de Estados Unidos para eliminar  la columna de pais y reducir aún mas los datos totales

Tambien podemos observar que los estados con mas instalaciones para vacunarse son Los Angeles, Orange, Montgomery y Cook. El medio de transporte mas visto es camina, mientras conducir y el transporte público ocupan un porcentaje bastante menor.
