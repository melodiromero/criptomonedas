# criptomonedas


## Índice
1. [Objetivos ](#id1)
4. [KPI's](#id2)
2. [Fuentes de datos](#id3)
3. [EDA - Análisis Exploratorio de Datos](#id4)
5. [Informe](#id5)
6. [Referencias](#id6)


## 1. Objetivo General:

Analizar la situación actual del sector de telecomunicaciones en Argentina, con el fin de identificar oportunidades de crecimiento y mejora en la calidad del servicio de conectividad a internet.

## 1.1. Objetivo Específicos:

>[!IMPORTANT]
>
>Impulsar la demanda de servicio de internet (en cualquier tecnología) en ciudades con potenciales clientes, en el período de un año.

>[!IMPORTANT]
>
>Expandir la tecnología de cablemodem a todas las ciudades argentinas que aún no lo possen en el término de un año.

>[!IMPORTANT]
>
>Expandir la tecnología de fibra óptica a todas las ciudades argentinas que carecen de esta tecnología en el periodo de tres años.

## 2. KPI's

Como idicadores claves de desempeño que ayuden a cumplimentar los objetivos propuestos, se han establecido los siguientes:

<ul>
<li> **Tasa de conversion de localidades actuales**. Tasas de conversión de los clientes que demanda (localidades que registran accesos) sobre el total de clientes interesados (localidades con y sin accesos). </li>
<li> **Total de accesos actuales ** (o en base al periodo 2022).</li>
<li> **Porcentaje de accesos con fibra óptica**.</li>
<li> **Porcentaje de accesos con cablemodem**.</li>
</ul>

De los ultimos dos, se relacionan los siguientes:
 - Número de clientes potenciales con acceso a fibra óptica.
 - Número de clientes potenciales sin acceso a fibra óptica.
 - Número de clientes potenciales con acceso a cablemodem.
 - Número de clientes potenciales sin acceso a cablemodem.


## 2. Fuente de datos
Se detallan las fuentes de datos obligatorias y complementarias utilizadas.

### 2.1. Datasets utilizados
Se hacen uso de los siguientes datas:

[Acceso de internet por tecnologías](datasets/Internet_Accesos-por-tecnologia.csv) y 
[acceso de internet por tecnologia y provincia](datasets/Internet_Accesos-por-tecnologiayporprovincia.csv)
Se analizaron estos datas con el fin de evaluar la situación actual de las telecomunicaciones en Argentina, al menos d elos ultimos registros datan del año 2022, 3er trimestr(Julio-Septiembre). 


[conectividad de internet](datasets/ConectividadalserviciodeInternet.csv) y [listado de localidades con conectividad a internet](datasets/Listadodelocalidadesconconectividadainternet.csv)
Con el fin de responder a nuestros KPI's se exploró este dataset, identificando oprotunidades de crecimiento. 

### 2.2. Fuentes adicionales
[listado de provincias](datasets/provincias.csv)
Se indagó este dataset en particular para obtener información acerca de la ubicación geográfica de cada provincia, mediante sus datos de latitud y longitud[^3].

### 2.3. Diccionario de datos: metadatos
| Nombre del campo | Descripción |
| --- | --- |
| dt | tipo de recurso: conjunto de datos. |
| ds | tipo de recurso: vistas. |
| vz | tipo de recurso: visualizaciones. |
| db | tipo de recurso: colecciones. |
| guid | Identificador del recurso. |
| title | Título del conjunto de datos. |
| description |  Descripción del conjunto de datos. |
| categories | Nombre de la categoría. |
| endpoint |  Url apuntando al recurso con los datos (archivos o página web). |
| tags |  Opcional. Tags separados por coma. |
| user |  Usuario que publica el recurso. |
| parameters |  Parámetros que tiene el recurso. |
| created_at |  Fecha de creación de la versión del recurso. |
| link |  Link a la vista del recurso en el portal. |

## 3. EDA - Análisis Exploratorio de Datos
Se realizó el análisis explotatorio de los datos para cada uno de los datasets previamente descargados en formato CSV. En cada eda, se analizan los datos, se describen los mismos, detectando outliers sin eliminarlos, se sigue por la descripción de la distribución de sus datos y se ofrecen visualizaciones que contribuyen a la labor de conclusiones que sean útiles para los indicadores de rendimientos y la toma de decisiones oportunas en la cumplimentación de los objetivos específicos. El análisis exploratorio de cada dataset se halla en la carpeta titulada "eda", contiene tres edas acerca de las tecnologias de acceso a internet y la conectividad de las mismas a lo largo de todo el territorio argentino.

## 5. Informe

En base a lo analizado, se concluye que **el servicio de internet más contratado es la modalidad de cable modem** y la minoría se representa por la categoría otros. 
<p align="center">
  <img width="600" height="350" src="graficos/evolucion_tecnologias.png">
</p>

<p align="center">
  <img width="600" height="300" src="graficos/distribucion_tecnologias_periodo2014_2022.png">
</p>

<p align="center">
  <img width="600" height="300" src="graficos/distribucion_tecnologias_anio2022.png">
</p>

Se observa que **a lo largo de los años, hubo un mayor crecimiento en la demanda de tecnología de acceso de internet por cable modem, con un 50% y fibra óptica con 37%**, no asi, en el caso de ADSL, que fue decreciendo. En sus inicios la modalidad que inicio fuertemente fue ADSL con cable modem, pero dado el último año (2022) se registra que la prominente es cabla módem (55%) y le sigue fibra óptica (24%).

En cuando a la categoria "otros", según la fuente del ENACOM[^2] y la exploración de la conectividad en el servicio de internet, en esta modalidad pueden incluirse los contratados por acceso telefónico (Dial-Up), acceso por red de telefonía móvil con 3G y 4G, y el acceso por linea eléctrica.

<p align="center">
  <img width="500" height="400" src="graficos/localidades con y sin servicio de internet.png">
</p>

<p align="center">
  <img width="500" height="400" src="graficos/localidades potenciales y el cablemodem.png">
</p>

<p align="center">
  <img width="500" height="400" src="graficos/localidades potenciales y la fibra optica.png">
</p>

En atención al objetivo de **Impulsar la demanda de servicio de internet (en cualquier tecnología) en ciudades con potenciales clientes, en el período de un año.** y los KPI's seleccionados, se detallan como métricas, el registro de 4307 localidades, de las cuales, 3765 son clientes y 542 son clientes potenciales. A qué se refiere con potenciales, pues que en estas localidades no hay una demanda en accesos de servicio de internet pero se cuentan con las tecnologías para aprovechar esta  **oportunidad de crecimiento** y **potenciar la demanda del servicio a internet**
En este documento se detallan las localidades potenciales:
[listado de localidades potenciales](datasets/conectividadlocalidades_oportunidadExpansion.csv)
Entonces como tasa de localidades clientes se tiene un 87% en contraste con los clientes potenciales que representan el 13%.

Finalmente para el logro de los objetivos de expandir la tecnología de cablemodem a todas las ciudades argentinas que aún no lo possen en el término de un año y expandir la tecnología de fibra óptica a todas las ciudades argentinas que carecen de esta tecnología en el período de tres años , esta última se ha propuesto en tres años debido al costo que implica esta tecnología, se han hallado los siguientes indicadores:

Para el cablemodem de las 542 localidades potenciales, 24, el 4% tienen potencial acceso por cablemodem y 518, el 96% no poseen acceso. Y para la fibra optica, de las 542 localidades potenciales, 76, el 14% tienen acceso a fibra óptica y 466, el 86% no poseen acceso.

En base al pase de los años y el crecimiento de estas tecnologías se concluye que es factible la realización de los objetivos propuestos.

## 6. Referencias
[^1]: El Enacom es un ente autárquico y descentralizado que funciona en el ámbito de la Jefatura de Gabinete de Ministros de la Nación Argentina. Su objetivo es conducir el proceso de convergencia tecnológica y crear condiciones estables de mercado para garantizar el acceso de todos los argentinos a los servicios de internet, telefonía fija y móvil, radio, postales y televisión.Enacom fue creado en Diciembre del 2015 a través del Decreto 267 en el cual se establece su rol como regulador de las comunicaciones con el fin de asegurar que todos los usuarios del país cuenten con servicios de calidad. Fuente: https://enacom.gob.ar/

[^2]: Tipos de acceso a internet https://www.enacom.gob.ar/tipos-de-conexion_p112

[^3]: Lista de las entidades que representan la división político territorial de primer orden de la República Argentina en base a datos del Instituto Geográfico Nacional y del Instituto Nacional de Estadística y Censos. Incluye las 23 provincias y la Ciudad Autónoma de Buenos Aires (CABA) en formato SHP. Fuente: https://datos.gob.ar/dataset/jgm-servicio-normalizacion-datos-geograficos/archivo/jgm_8.26