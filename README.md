# criptomonedas

Análisis exploratorio del mercado de criptomonedas utilizando datos de la API CoinGecko, con el fin de descubrir tendencias, hallazgos que contribuyan a la toma de decisiones.

## Índice
1. [KPI's ](#id1)
2. [Fuentes de datos](#id3)
3. [EDA - Análisis Exploratorio de Datos](#id4)
5. [Informe](#id5)

## 1. KPI's

>[!IMPORTANT]
>
>Aumentar la inversión del bitcoin en un 15% para el próximo mes.

>[!IMPORTANT]
>Aumentar la inversión del Tether (USDT) en un 10% para el próximo mes.
>.

>[!IMPORTANT]
>
>Realizar una inversion de 100 millones en un smart contract, (el más favorable),para el próximo mes.

## 2. Fuente de datos

[API CoinGecko](https://www.coingecko.com/es/api/documentation)

 - Endpoint: **GET coins/market** para otener el listado de todas las monedas con lo datos del mercado de monedas (precio, capitalización de mercado, volumen). 


**Diccionario de Datos**

market_cap
| Columna | Descripción  |
|:------------- |:-------------| 
| id         | Clave primaria de la moneda          | 
| symb         | Símbolo de la moneda         |
| name         | Nombre de la criptomoneda          |
| image         | url donde se halla una imagen ilustrativa que representa la cripto          |
| current_price | Precio actual         |
| market_cap         | Capitalización del mercado. Precio de la Criptomoneda × Cantidad Total de Criptomoneda en Circulación. Donde "Precio de la Criptomoneda" es el precio actual de una unidad de la criptomoneda y "Cantidad Total de Criptomoneda en Circulación" es la cantidad total de unidades de esa criptomoneda que están siendo negociadas en el mercado.          |
| market_cap_rank         | El rango de capitalización de mercado de una criptomoneda se refiere a la posición relativa de esa criptomoneda en comparación con otras criptomonedas en función de su capitalización de mercado.         |
| fully_diluted_valuation         |  La valoración totalmente diluida es una representación estadística del valor máximo de un proyecto de criptomoneda, suponiendo que todos sus tokens ya estén en circulación. FDV = Precio actual x Cantidad máxima (o cantidad total si la cantidad máxima no es válida). La capitalización de mercado (valoración) si la cantidad máxima de una moneda está en circulación. Tenga en cuenta que pueden pasar 3, 5, 10 o más años hasta que se alcance el FDV según el calendario de emisión.     |
| total_volume         | Se refiere a la cantidad total de una criptomoneda que se ha negociado en un período de tiempo específico, generalmente en un día. Es la suma de todas las transacciones realizadas en esa criptomoneda durante ese período. El volumen es una métrica crítica en el análisis técnico y fundamental, ya que indica la actividad comercial y la liquidez de una criptomoneda. Un alto volumen puede indicar un interés significativo y una alta liquidez, mientras que un volumen bajo podría sugerir una actividad comercial limitada. |
| high_24h         |Máximo en 24 |
| low_24h         | Mínimo en 24 |
| price_change_24h              | Cambio de precio en 24h|
| price_change_percentage_24h         | Porcentaje del cambio de precio en 24h |
| market_cap_change_24h         | Cambio de la capitalización de mercado en 24hs | 
| market_cap_change_percentage_24h         | Porcentaje de la cambio de la capitalización de mercado en 24hs |
| circulating_supply     | Este campo representa la cantidad de la criptomoneda que está actualmente en circulación y en manos de los inversores. |
| total_supply     | Este campo representa la cantidad total de la criptomoneda que existe en el momento actual, incluyendo la que está en circulación y la que aún no ha sido liberada. | 
| max_supply         | Este campo representa la cantidad máxima posible de la criptomoneda que podría existir en total. No todas las criptomonedas tienen un suministro máximo definido. |
| ath |  "ATH" significa "All-Time High" en inglés, que se traduce como "Máximo Histórico" en español. Se refiere al precio más alto jamás alcanzado por una criptomoned.| 
| ath_change_percentage         | Este es el porcentaje de cambio que representa la diferencia entre el precio actual de una criptomoneda y su máximo histórico (ATH), expresado como un porcentaje. | 
| ath_date        | Esta es la fecha en la que la criptomoneda alcanzó su máximo histórico (ATH). Indica cuándo se registró el precio más alto para esa criptomoneda. |
| atl      |   "ATL" significa "All-Time Low", que se traduce como "Mínimo Histórico" en español. Se refiere al precio más bajo jamás alcanzado por una criptomoneda. |
| atl_change_percentage       | Este es el porcentaje de cambio que representa la diferencia entre el precio actual de una criptomoneda y su mínimo histórico (ATL), expresado como un porcentaje.  |
| atl_date      |  Esta es la fecha en la que la criptomoneda alcanzó su mínimo histórico (ATL). Indica cuándo se registró el precio más bajo para esa criptomoneda. |
| roi     |  El ROI es una métrica que indica la rentabilidad de una inversión en función de la ganancia generada en relación con el costo inicial de la inversión. El ROI te proporciona información sobre el rendimiento de tu inversión en términos porcentuales. Un ROI positivo indica que has obtenido ganancias, mientras que un ROI negativo indica pérdidas.|
| last_updated     |  Última actualización |
| roi.times     | Esta expresión podría hacer referencia a la cantidad de veces que el ROI excede el costo inicial de la inversión. Por ejemplo, si el ROI es 2, significa que la inversión ha duplicado su valor.  |
| roi.currency     |   Esta expresión se refiere a la moneda en la que se está calculando el ROI. Dado que las criptomonedas y las inversiones pueden estar denominadas en diferentes monedas, esta propiedad podría indicar la moneda específica en la que se está realizando el cálculo del ROI.|
| roi.percentage     |  Esto probablemente se refiere a la representación del ROI en forma de porcentaje. El ROI se expresa comúnmente en términos porcentuales para indicar cuánto ha aumentado o disminuido el valor de la inversión en relación con su costo inicial.  |

## 3. EDA - Análisis Exploratorio de Datos
ver.....Se realizó el análisis explotatorio de los datos para cada uno de los datasets previamente descargados en formato CSV. En cada eda, se analizan los datos, se describen los mismos, detectando outliers sin eliminarlos, se sigue por la descripción de la distribución de sus datos y se ofrecen visualizaciones que contribuyen a la labor de conclusiones que sean útiles para los indicadores de rendimientos y la toma de decisiones oportunas en la cumplimentación de los objetivos específicos. El análisis exploratorio de cada dataset se halla en la carpeta titulada "eda", contiene tres edas acerca de las tecnologias de acceso a internet y la conectividad de las mismas a lo largo de todo el territorio argentino.

## 5. Informe
