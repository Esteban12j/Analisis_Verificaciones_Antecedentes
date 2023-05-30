30-5-2023

Analista de Identidad: Esteban Quengúan 

FAST-MARKET

Informe de Análisis de Verificaciones de Antecedentes de Gigsters
![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.001.png)![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.002.png)![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.003.png)


# Contenido
[Resumen	2](#_toc136340643)

[Introducción	3](#_toc136340644)

[Metodología de análisis	4](#_toc136340645)

[Análisis e Informes	5](#_toc136340646)

[Distribución de Puntuación	5](#_toc136340647)

[Número de Checks con Posible Fraude	5](#_toc136340648)

[Tasa de Aceptación / Rechazo	6](#_toc136340649)

[Razones más Comunes de Rechazo	7](#_toc136340650)

[Correlación entre Score y Score criminal background	7](#_toc136340651)

[Gráfico de distribución de puntuación por conjunto de datos	7](#_toc136340652)

[Tabla de frecuencia de keywords_criminal	8](#_toc136340653)

[Recomendaciones	9](#_toc136340654)

[Conclusiones	10](#_toc136340655)


# Tablas

[Tabla 1:Registros con scores en cero	7](#_toc136340069)

[Tabla 2: Frecuencia de Medidas Cautelares	9](#_toc136340070)
# ` `Ilustraciones
[Ilustración 1: distribución de puntuación	6](#_toc136339942)

[Ilustración 2: Gisters con score de cero	7](#_toc136339943)

[Ilustración 3: Histograma de medidas cautelares con Mora	8](#_toc136339944)

[Ilustración 4: Mapa de correlación	8](#_toc136339945)

[Ilustración 5: Distribución de puntuación por conjunto de datos	9](#_toc136339946)






# <a name="_toc136340643"></a>Resumen

- El análisis de los datos de los Gigsters revela que la mayoría de ellos tienen puntuaciones altas, indicando la falta de antecedentes penales, multas de tránsito o problemas financieros.
- Se identificaron Gigsters con puntuaciones bajas (0.0, 0.05), sugiriendo la necesidad de verificaciones adicionales para detectar posibles problemas de identidad o antecedentes penales.
- Es importante abordar los problemas de precisión decimal en las puntuaciones para garantizar una representación más precisa de los datos.
- Se detectaron casos de posibles fraudes o datos incompletos, por lo que se recomienda consultar fuentes adicionales o verificar la calidad y confiabilidad de los datos.
- El porcentaje de Gigsters con posibles fraudes es del 0.54%, lo que destaca la importancia de una verificación minuciosa.
- La tasa global de aceptación de los Gigsters es del 64.23%, mientras que la tasa de rechazo es del 35.77%.
- Se encontraron 69 registros con puntuaciones superiores a 0.8, indicando una alta confiabilidad en antecedentes penales y financieros.
- Se identificaron 306 registros con puntuaciones inferiores a 0.8, requiriendo una evaluación adicional antes de su aceptación.
- Los delitos más comunes en los antecedentes criminales de los Gigsters son el "abuso de confianza" y las "sanciones".
- Se recomienda a Fast-Market seguir utilizando los servicios de verificación de antecedentes de [Xempresa], pero se deben considerar los puntos mencionados anteriormente para tomar decisiones informadas y garantizar la seguridad y confiabilidad de los Gigsters contratados.


# <a name="_toc136340644"></a>Introducción
Este informe tiene como objetivo proporcionarle una visión detallada de los resultados obtenidos, así como las recomendaciones clave para mejorar el proceso de selección de Gigsters en Fast-Market.

En un entorno laboral en constante evolución, es fundamental contar con una estrategia sólida para garantizar la seguridad y la confianza en la contratación de personal. La verificación de antecedentes es una práctica efectiva para mitigar riesgos y tomar decisiones informadas. En este informe, se analizaron los conjuntos de datos proporcionados por [Xempresa], que incluyen antecedentes penales, multas de tránsito y antecedentes financieros de los Gigsters.

A lo largo de este informe, se explorarán diversos aspectos, como la distribución de puntuaciones, el análisis de posibles fraudes, las tasas de aceptación y rechazo, así como las razones comunes de rechazo. Además, se presentarán recomendaciones específicas sobre cómo utilizar los resultados del análisis para mejorar el proceso de selección de Gigsters y fortalecer la seguridad y la confianza en Fast-Market.

Agradecemos su confianza en nuestros servicios y esperamos que este informe le proporcione información valiosa para tomar decisiones informadas y mejorar la eficiencia y calidad de su proceso de selección de Gigsters.



<a name="_toc136340645"></a>Metodología de análisis

1. Importar la biblioteca pandas para el análisis de datos:
1. Leer el archivo de Excel que contiene los datos:
1. Asumimos que los Gisters activados son aquellos que tienen una puntuación global de 0.8 en adelante
1. Realizar el análisis exploratorio de los datos:
- Histograma y Boxplot del score:
- Se generan gráficas para visualizar la distribución de las puntuaciones de los Gigsters.
1. Identificación de posibles fraudes:
- Se crea un nuevo DataFrame con los usuarios que tienen "not\_found" en el campo "identity\_status".
- Se generan gráficas para visualizar la distribución de las puntuaciones de los Gigsters con "not\_found" en "identity\_status".
1. Criterio de aceptación y rechazo:
- Criterio de aceptación: Gigsters con una puntuación global igual o mayor a 0.8.
- Criterio de rechazo: Gigsters con una puntuación global inferior a 0.8.
1. Análisis de los registros financieros:
- Se crea un nuevo DataFrame con los registros que no son "SIN MORA" o tienen un valor no nulo en el campo "financial\_status".
- Se realiza el conteo y porcentaje de registros con puntuación mayor o igual a 0.8 y menor a 0.8, sin mora.
1. Análisis de los registros aceptados pero con "keywords\_criminal":
- Se crea un nuevo DataFrame con los registros que tienen una puntuación mayor o igual a 0.8 y "keywords\_criminal" no vacíos.
- Se realiza el conteo de registros con "keywords\_criminal" no vacíos y se genera un histograma.


# <a name="_toc136340646"></a>Análisis e Informes

## <a name="_toc136340647"></a>Distribución de Puntuación
La distribución de puntuación proporciona información importante sobre el nivel de confiabilidad de los Gigsters. A continuación, se muestra un histograma que muestra la frecuencia de diferentes puntuaciones obtenidas por los Gigsters:

![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.004.png)

<a name="_toc136339942"></a>*Ilustración 1: distribución de puntuación*

Del análisis de la distribución de puntuación, se observa que la mayoría de los Gigsters obtienen puntuaciones altas, con un pico significativo alrededor de 0.75. Sin embargo, también se identifican algunos casos con puntuaciones bajas, lo que indica la presencia de posibles riesgos.

## <a name="_toc136340648"></a>Número de Checks con Posible Fraude
Al analizar los datos, se identificaron Gigsters con posibles indicios de fraude. Estos casos se caracterizan por la presencia de campos vacíos o información inconsistente. En particular, se encontraron 7 checks con posible fraude, como se muestra a continuación:

![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.005.png)

<a name="_toc136339943"></a>*Ilustración 2: Gisters con score de cero*

<a name="_toc136340069"></a>*Tabla 1:Registros con scores en cero*

|**score**|**score\_ criminal\_background**|**keywords\_ criminal**|**score\_ traffic\_fines**|**fines\_ count**|<p>**score\_**</p><p>**financial\_**</p><p>**background**</p>|<p>**financial\_**</p><p>**status**</p>|
| :- | :- | :- | :- | :- | :- | :- |
|**0.0**|0\.0|NaN|0\.0|NaN|0\.0|NaN|

Es esencial investigar y evaluar cuidadosamente estos casos para garantizar la integridad y confiabilidad de los Gigsters contratados.

## <a name="_toc136340649"></a>Tasa de Aceptación / Rechazo
La tasa de aceptación y rechazo es un indicador clave para evaluar la efectividad del proceso de selección. En el análisis de los datos, se obtuvieron los siguientes resultados:

- Tasa de aceptación: 64.23%
- Tasa de rechazo: 35.77%

Esto implica que la mayoría de los Gigsters verificados cumplieron con los criterios establecidos, pero aún existe una proporción significativa que no cumplió con los requisitos o presentó posibles riesgos.

<a name="_toc136340650"></a><a name="_toc136339944"></a>*Ilustración 3: Histograma de medidas cautelares con Mora*
## ![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.006.png)![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.007.png)Razones más Comunes de Rechazo
Al revisar los casos de rechazo, se identificaron ciertas razones recurrentes. Se encontró que el 65% de los Gigsters rechazados presentaban mora en sus antecedentes financieros. 

Además, se identificaron 54 Gigsters aceptados que tenían la palabra clave "Medidas cautelares, Abuso de confianza, Sanción y hostigamiento" en sus registros.




## <a name="_toc136340651"></a>Correlación entre Score y Score criminal background
<a name="_toc136339945"></a>*Ilustración 4: Mapa de correlación*
![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.008.png)![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.009.png)

Se realizó un mapa de correlación de calor para evaluar la relación entre la puntuación general (score) y el antecedente criminal (score\_criminal\_background). Se encontró una correlación positiva significativa de 0.88 entre estas dos variables, lo que indica que el antecedente criminal juega un papel importante en la determinación de la puntuación general.






## <a name="_toc136340652"></a>Gráfico de distribución de puntuación por conjunto de datos 

<a name="_toc136339946"></a>*Ilustración 5: Distribución de puntuación por conjunto de datos*
![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.010.png)![](Aspose.Words.73c20c80-a168-493f-89ea-72a667c8248c.011.png)Este gráfico muestra la distribución de puntuación para cada uno de los conjuntos de datos (Criminal Background, Traffic Fines, Financial Background). 









1. La mayoría de los Gigsters verificados presentan puntuaciones altas en los tres conjuntos de datos (Antecedentes Criminales, Multas de Tránsito y Antecedentes Financieros). Esto se refleja en la presencia de una caja grande en la parte derecha del gráfico, entre 0.8 y 1. Este patrón indica que la mayoría de los Gigsters no tienen antecedentes criminales, multas de tránsito significativas o problemas financieros graves.

1. Existe una variabilidad moderada en las puntuaciones de los Gigsters en los conjuntos de datos. Esto se representa mediante la presencia de una raya en el punto 0.6 en el gráfico. Esta variabilidad indica que algunos Gigsters pueden tener antecedentes criminales, multas de tránsito o situaciones financieras moderadas.

1. Se identificaron casos excepcionales donde los Gigsters obtuvieron puntuaciones bajas en los conjuntos de datos. Estos casos se representan mediante tres puntos ubicados en 0.4, 0.2 y 0.0 en el gráfico. Estos puntos indican la presencia de Gigsters con antecedentes criminales, multas de tránsito o situaciones financieras problemáticas que deben ser evaluados cuidadosamente en el proceso de selección.

## <a name="_toc136340653"></a>Tabla de frecuencia de keywords\_criminal
Esta tabla muestra la frecuencia de las palabras clave más comunes relacionadas con crímenes en los registros de los Gigsters. Ayuda a identificar los delitos más recurrentes y a enfocar los esfuerzos de verificación en áreas específicas.

<a name="_toc136340070"></a>*Tabla 2: Frecuencia de Medidas Cautelares*

|**keywords\_criminal**|**count**|**keywords\_criminal**|**count**|
| - | - | - | - |
|ABUSO DE CONFIANZA|62|EXTORSION|3|
|SANCION|53|MOTIN|3|
|ARMA DE FUEGO|37|ABUSO DE FUNCIONES|3|
|DELINCUENCIA ORGANIZADA|32|USUARPACION|2|
|HOMICIDIO DOLOSO|26|DIFAMACION|2|
|ROBO|21|AMENAZAS|2|
|MEDIDAS CAUTELARES|14|ENCUBRIMIENTO|2|
|NARCOTRAFICO|13|PEDERASTIA|2|
|VIOLACION|12|TERRORISMO|2|
|HOSTIGAMIENTO|12|ALLANAMIENTO|2|
|VIOLENCIA FAMILIAR|8|FRAUDE|2|
|ROBO A TRANSPORTE DE CARGA|7|FEMINICIDIO|2|
|TORTURA|6|INFANTICIDIO|2|
|HOMICIDIO CULPOSO|6|DESAPARICION FORZADA|2|
|SABOTAJE|5|ABANDONO|1|
|SECUESTRO|5|PIRATERIA|1|
|DAÑO EN PROPIEDAD AJENA|5|LESIONES|1|
|FALSIFICACION|4|TURISMO SEXUAL|1|
|TRATA DE PERSONAS|4|REBELION|1|
|CALUMNIA|4|CONSPIRACION|1|
|EXPLOSIVOS|4|GOLPES|1|
|GENOCIDIO|4|PROVOCACION|1|



# <a name="_toc136340654"></a>Recomendaciones
Basado en los resultados del análisis y los hallazgos identificados, se hacen las siguientes recomendaciones para mejorar el proceso de selección de Gigsters:

1. Revisar y actualizar los criterios de aceptación/rechazo: Considerar ajustar los criterios utilizados para evaluar a los Gigsters, teniendo en cuenta los resultados del análisis y las razones comunes de rechazo. Esto puede incluir la modificación de los umbrales de puntuación y la incorporación de nuevos criterios relevantes.

1. Realizar verificaciones adicionales: Considerar la implementación de verificaciones adicionales, especialmente para los Gigsters con puntuaciones bajas o con posibles indicios de fraude. Esto puede incluir la verificación manual de información, la solicitud de documentación adicional o la realización de entrevistas personales.

1. Reforzar la verificación de antecedentes financieros: Dado que la presencia de mora en los antecedentes financieros fue una razón común de rechazo, se recomienda prestar especial atención a este aspecto durante el proceso de selección. Esto puede incluir una verificación más exhaustiva de los antecedentes financieros y establecer criterios claros para evaluar la morosidad.

1. Capacitar al personal de selección: Proporcionar capacitación adecuada al personal encargado de la selección de Gigsters, para que puedan interpretar y utilizar eficientemente los resultados de las verificaciones de Xempresa. Esto ayudará a garantizar una evaluación precisa y consistente de los candidatos.

1. Monitorear continuamente el desempeño del proceso de selección: Establecer un sistema de seguimiento y monitoreo para evaluar regularmente el desempeño del proceso de selección de Gigsters, identificar áreas de mejora y realizar ajustes necesarios para optimizar los resultados.

# <a name="_toc136340655"></a>Conclusiones
En conclusión, el análisis de los datos de verificación de Gigsters utilizando Xempresa proporciona información valiosa para mejorar el proceso de selección y mitigar posibles riesgos asociados con la contratación de personal. A partir de los resultados del análisis, se pueden extraer las siguientes conclusiones clave:

1. La mayoría de los Gigsters verificados obtienen puntuaciones altas, lo que indica un nivel general de confiabilidad. Sin embargo, también se identificaron casos con puntuaciones bajas, lo que resalta la importancia de evaluar cuidadosamente a cada candidato.
1. Se encontraron casos con posibles indicios de fraude, como campos vacíos o información inconsistente. Estos casos deben ser investigados y evaluados exhaustivamente para garantizar la integridad del proceso de selección.
1. Existe una correlación significativa entre la puntuación general y el antecedente criminal, lo que destaca la relevancia de considerar este aspecto al evaluar la confiabilidad de los Gigsters.
1. Se identificaron razones comunes de rechazo, como la presencia de mora en los antecedentes financieros y ciertas palabras clave relacionadas con crímenes. Estas razones deben ser consideradas al establecer criterios de aceptación/rechazo y al realizar verificaciones adicionales.
1. Se recomienda ajustar los criterios de selección, realizar verificaciones adicionales y brindar capacitación al personal de selección para mejorar el proceso de selección y garantizar una evaluación más precisa de los Gigsters.
