# Selección de datos
Seleccionamos los datos de acceso en un tiempo determinado desde ciertas zonas a centros vacunatorios para covid-19 en Estados Unidos, Puerto Rico y las islas virgenes de Estados Unidos entre junio de 2021 y septiembre de 2022 que están disponibles en Google Cloud.

Esto nos dará una percepción para comparar la conectividad que presentan distintos estados y paises, junto a generar hipotesis acerca de las preferencias de sus planificaciones urbanas, ya que se presentan distintos medios para acercarse.

Los datos se obtuvieron de: https://console.cloud.google.com/marketplace/product/bigquery-public-datasets/covid19-vaccination-access


## Datos
Los datos estan separados por una tabla para cada medio de transporte y una tabla que acumula todos. Se carga la tabla que contiene los datos de todos y se utiliza BigQuery para poder visualizarlos:

![Datos brutos](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Datos%20brutos.png)

De esta forma se pueden eliminar las columnas de datos que son redundantes, en este caso hay varias columnas referentes a las posición e identificación de las instalaciones de vacunación que se pueden eliminar por este motivo. Así las columnas que se presentarían despues de limpiar son: nombre de la instalación, pais, estado/subregión, medio de transporte y tiempo de viaje.
Esto reduce la tabla de 15 a 5 columnas, haciendo que sea mas facil gestionar la información.

 Si observamos el conteo de paises podemos darnos cuenta de algo interesante:

![Conteo de paises](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Conteo%20de%20paises.png)

Estados Unidos corresponde a un 99,62% de los datos totales, por lo que podemos tomar toda la data de Estados Unidos para eliminar  la columna de pais y reducir aún mas los datos totales.

Con los datos reducidos, se realiza un query que cumpla los requisitos mencionados y obtenemos una tabla mas manejable:

![Datos limpios](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Datos%20limpios.png)

Podemos realizar una mejor observación contando las veces que se repiten nombres o valores por cada columna:

![Conteo de datos](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Conteo%20de%20datos.png)

Vemos ciertos nombres que se repiten bastante(En el código están los datos totalmente desplegados), por ejemplo, en los nombres de la instalación se repiten mucho los nombres CVS Pharmacy, Walgreens Pharmacy, Walmart y Rite Aid.

Tambien podemos observar que los estados con mas instalaciones para vacunarse son Los Angeles, California, Nueva York. El medio de transporte mas visto es caminar, mientras conducir y el transporte público ocupan un porcentaje bastante menor.

## Gráficas

Realizamos un Pie Chart para poder visualizar la proporción de los nombres de las 5 instalaciones mas repetidos:

California:

![Grafico Pie Modos California](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Grafico%20Pie%20Modos%20California.png)

Nueva York:

![Grafico Pie Modos Nueva York](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Grafico%20Pie%20Modos%20Nueva%20York.png)

Florida:

![Grafico Pie Modos Florida](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Grafico%20Pie%20Modos%20Florida.png)

Es claramente visible que la principal distribuidora en estos estados es CVS Pharmacy, mientras Wallgreens Pharmacy tambien se presenta en todos los estados. El resto de instalaciones que no ocupan estos nombres equivalen a un menos del 30%.

Aprovechando esta selección de estados, tambien veamos como se comparan las cantidades de rutas por medio de transporte:

![Sunburst 3 datos](https://github.com/VicenteLizana/Solemne1/blob/master/Imagenes/Sunburst%203%20datos.png)

Es claramente visible que California es el estado con mas instalaciones, le sigue Nueva York y Florida. Otro detalle que podemos ver es que el caminar es el medio que mas rutas posee, lo que a priori podría significar que estos estados permiten una movilidad cómoda al caminar para encontrar una instalación dónde vacunarse.



![Barras horizontales]()