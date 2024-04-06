<!--# Solemne 1 Minería de Datos 2024-->
# Análisis de datos sobre COVID-19 y su impacto

## Objetivos

Se espera que los alumnos muestren conocimiento en las siguientes áreas:

- Realizar consultas a bases de datos públicas alojadas en Google Cloud Platform
- Consumir y procesar datos de APIs públicas
- Trabajar con bases de datos relacionales y datos en formato JSON
- Limpieza, transformación y combinación de datos
- Visualización de datos
- Interpretación y narración de hallazgos
- Versionado de software y colaboración en GitHub

## Instrucciones

Utilizando los conjuntos de datos públicos relacionados con COVID-19 disponibles en BigQuery y APIs relevantes, se pide realizar lo siguiente:

1. Exploración de datos:
    - Identificar un conjunto de datos públicos en BigQuery y una API pública relacionados con COVID-19 (por ejemplo, datos de casos, vacunación, movilidad, etc.).
    - Realizar consultas SQL y consumir datos de la API para explorar y comprender las características de los conjuntos de datos seleccionados.
2. Limpieza y transformación de datos:
    - Cargar los datos obtenidos en DataFrames de Pandas.
    - Realizar tareas de limpieza, transformación y combinación de datos según sea necesario, utilizando las capacidades de Pandas.
3. Visualización de datos:
    - Crear al menos cinco visualizaciones diferentes (gráficos de líneas, barras, dispersión, mapas, etc.) utilizando Matplotlib y/o otras bibliotecas de visualización, que muestren insights interesantes sobre los datos de COVID-19 y su impacto.
    - Las visualizaciones deben estar bien etiquetadas, con títulos, ejes y leyendas claras.
4. Análisis e interpretación de resultados:
    - Realizar un análisis exhaustivo de los datos, resaltando los hallazgos más relevantes y las tendencias observadas.
    - Interpretar los resultados y proporcionar explicaciones claras sobre los insights derivados de las visualizaciones y las técnicas de minería de datos aplicadas.
5. Entrega y documentación:
    - Crear un repositorio en GitHub para este proyecto.
    - Realizar commits regulares, con mensajes descriptivos, a medida que avancen en el proyecto.
    - Utilizar una rama de desarrollo y una rama de producción, realizando las correspondientes fusiones de solicitudes de extracción (pull requests).
    - Redactar un informe en formato Markdown o Jupyter Notebook que describa el proceso de análisis, los hallazgos más relevantes y las conclusiones obtenidas.
    - Incluir un archivo requirements.txt que liste las librerías de Python relevantes para el desarrollo del análisis.
    - Proporcionar un archivo README.md que presente los resultados obtenidos, indicando y argumentando todos los descubrimientos realizados en los datos.

## Evaluación

La prueba será evaluada según los siguientes criterios:

- Calidad y exhaustividad del análisis de datos (2 puntos)
- Claridad y efectividad de las visualizaciones (2 puntos)
- Interpretación y narración de hallazgos (1 punto)
- Uso adecuado de GitHub y buenas prácticas de versionado de software (1 punto)
- Documentación y presentación de resultados (1 punto)

Puntaje total: 7 puntos

## Recursos adicionales

- [Guía de buenas prácticas para trabajar con Git](https://david-estevez.gitbooks.io/the-git-the-bad-and-the-ugly/content/es/buenas-practicas-al-trabajar-con-git.html)
- [Conjuntos de datos públicos de COVID-19 en BigQuery](https://console.cloud.google.com/marketplace/browse?filter=solution-type:dataset&q=covid)
- [APIs públicas relacionadas con COVID-19](https://github.com/public-apis/public-apis#health)

Si van a trabajar en grupos, cada integrante debe tener su rama de desarrollo y hacer los correspondientes fork y pull requests. Asegúrense de especificar los integrantes del grupo en el archivo README.md.

¡Feliz prueba!
