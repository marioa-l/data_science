# Estimación de Métricas de Estructura y Complejidad de Programas Lógicos Rebatibles

## Proyecto Final de la Especialización en Ciencias de Datos 2022

En este proyecto se usaron clasificadores y autoencoders con el objetivo de hacer escalable el proceso de generar y evaluar valores de parámetros que sirven para generar programas PreDeLP con DPG. Para hacer escalable el proceso de evaluar valores de parámetros, se definió y entrenó un conjunto de clasificadores dando como resultado un clasificador SVC con valores de métricas aceptables. Para escalar el proceso de generación de valores de parámetros que permitan construir programas PreDeLP fáciles o difı́ciles según el tiempo de respuesta a consultas, se utilizaron dos tipos de autoencoders, uno que aprende en base al conjunto de todos los parámetros a la vez, y otro que aprender la distribución de valores de cada parámetro por separado.

El dataset usado fue generado de manera sintética con el Generado de Programas PreDeLP [DPG](https://github.com/marioa-l/DeLP-Gen.git) y computando el valor de todas las métricas para cada programa, junto con el tiempo promedio para responder todos los literales del programa. Cada fila del dataset representa:

- Un programa PreDeLP.
- El conjunto de parámetros con los que fue generado el programa:
	- $\mathtt{BE, FACTS, DRUL, HEADS, BODY, ARGLVL, LVL, DEFT, HEIGHT}$.
- El valor de sus métricas:
	- $\mathtt{NRU, NBE, NAR, NDT, ALE, AWI, AHE}$.
- El tiempo promedio para responder el estado de todos los literales del programa: $\mathtt{Time}$.

El mismo contiene los datos de **32000** programas. Su estructura es la siguiente:

|Id                |Significado                          |Tipo                         |
|----------------|-------------------------------|-----------------------------|
|`programa`|Número de programa            |`int`            |
|`BE`|Número mı́nimo de hechos y presunciones            |`int`            |
|`FACTS`|Porcentaje de hechos            |`double`            |
|`DRUL`|Porcentaje de reglas rebatibles            |`double`            |
|`HEADS`|Máximo número de reglas con la misma conclusión            |`int`            |
|`BODY`|Máximo número de literales del cuerpo de un argumento            |`int`            |
|`ARGLVL`|Mı́nimo número de argumentos distintos por nivel            |`int`            |
|`LVL`|Máximo nivel de un argumento            |`int`            |
|`DEFT`|Máximo número de derrotadores para un argumento            |`int`            |
|`HEIGHT`|Altura de los árboles de dialéctica            |`int`            |
|`NRU`| Número de reglas (estrictias y rebatibles)            |`int`            |
|`NBE`|Número de hechos y presunciones            |`int`            |
|`NAR`|Número de argumentos            |`int`            |
|`NDT`|Número de árboles de dialéctica            |`int`            |
|`ALE`|Longitud promedio de un argumento            |`double`            |
|`AWI`|Ancho promedio de los árboles de dialéctica            |`double`            |
|`AHE`|Altura promedio de los árboles de dialéctica            |`double`            |
|`Time`|Tiempo promedio para consultar por todos los literales            |`double`            |

En este repositorio se encuentran disponible la notebook del proyecto, el conjunto de datos y los archivos con los resultados de las evaluaciones.