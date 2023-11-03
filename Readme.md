# <center> CAL CENTER </center>

![N|Solid](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSyWEMAsO2fStc8YIGr9f-co5h7D84aCB_E0A&usqp=CAU)
## - OBJETIVO
<i> El propósito de este trabajo es describir las operaciones del Call Center  de un Banco: “Anonymous Bank”, en función de las variables del negocio y proponer mejoras para el segmento premium de clientes.</i>


## - INTRODUCCIÓN

Analizar las operaciones de un Call Center de un Banco, para proponer mejoras en:
* Eficiencia operativa, proponiendo mejoras operativas.
* Mejorar la satisfacción del cliente, cumpliendo los SLA comprometidos.
* Brindar una herramienta para la gestión y la toma de decisiones del Call Center.

## - DESCRIPCIÓN
- En la primera etapa (E: Extracción) del proceso ETL,se realizó la extracción de datos desde su fuente de origen, archivo CSV. se utilizó al biblioteca Pandas, Numpy y herramientas de Python. 
  
-  En la segunda etapa (T: Transformación) del proceso, aplicamos diversas operaciones y reglas para limpiar, enriquecer y dar formato a los datos según nuestras necesidades. Se toma conocimiento de cantidad de columnas(18), filas(444448), valores nulos (0), y demás anomalias a simple vista.
Luego analizar el tipo de dato que contienen las columnas (variables) y se procede a su clasificación. observamos su comportamiento con describe(). 
Observamos que la columna id_call, sus valores deberian ser únicos ya que representan cada registro. Pero se observan duplicados, lo que se procede a cambiar y darle un valor único. Luego se elimina esa columna para evitar confusiones. 
También la columna startdate, no es descripta en el diccionario que se nos proporciona, por lo cual se considera insignificante y se elimina.

- En la tercer y última etapa (L: Load/Carga), se procede a la carga de los datos transformados en un CSV, ya limpios.

Con los datos limpios procedemos a realizar el EDA (Analisis de Datos Exploratorio)
- Adquisición de Datos: 
  
- Exploración de Datos Básica: Se estudió cada columna y su comportamiento

- Limpieza de Datos: Se identificó y se trató los valores duplicados y atípicos. Esto implicó eliminar registros y corregir errores en los datos.

- Resumen Estadístico: Se calculó estadísticas descriptivas como la media, la mediana, la desviación estándar y los percentiles para comprender mejor la distribución de los datos numéricos.

- Visualización de Datos: Se utilizó gráficos como histogramas, diagramas de caja, gráficos de dispersión y diagramas de barras para visualizar las características y relaciones de los datos para identificar patrones y tendencias.

- Segmentación y Agrupación: Se pueden crear grupos o segmentos de datos basados en características comunes. Esto puede ayudar a entender mejor la estructura de los datos y a identificar subconjuntos de interés.

- Análisis de Outliers: Se identificó y se analizó valores atípicos que pueden afectar las conclusiones del análisis.

 ## - CONCLUSIÓN

Según las preguntas presentadas para poder llegar a una conclusión del funcionamiento del Call Center, podemos decir:

  1) <u> Nivel de servicio - Clientes Prioritarios (Prioridad=2):</u> la mitad tuvo una atención de inmediato y el resto esperó solo unos 27 segundos.
  2) <u>Calidad respercto al servicio Normal:</u> al ingresar ya se los considera de forma diferente dandole mejor tiempo de espera y se observa que son atendidos en un promedio de 160 segundos.
  3) <u>Volumen de llamadas atendidas:</u> Se atienden en promedio 37.000 llamados por mes.
  4) <u>Clientes recurrentes en el uso del servicio:</u> Se encontró que el 65% de los clientes fueron atendidos por un agente entre 1 a 5 veces en todo el período analizado. 
  5) <u>Tipos de servicio más recurrentes:</u>  68% de los clientes son atendidos por Actividades Regulares(PS).

##RECOMENDACIONES

1) Reveer los datos suministrados en la columna Server por falta de datos o datos no muy claros como NO_SERVER.

2) Tener maximo cuidado al ingreso de las horas de entrada y salida, suelen estar cambiadas.

3) Analizar las llamadas que abandonan el Horario de LLAMADA.

4) Se podria dar la opción que al final de la llamada el cliente de un puntaje de satisfacción.
   
5) Analizar si es conveniente agregar personal en las horas picos para bajar el tiempo de espera tanto a los clientes premium como a los comunes.

Se añade un Dashboard para la visualizacion de las principales métricas y gráficas que verifican la calidad de atención del Call Center

![Alt text](image.png)