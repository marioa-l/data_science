# Estructura del dataset

El dataset a usar fue generado de manera sintética con el Generado de Programas PreDeLP (DPG) y computando el valor de todas las métricas para cada programa, junto con el tiempo promedio para responder todos los literales del programa. Cada fila del dataset representa:

- Un programa PreDeLP.
- El conjunto de parámetros con los que fue generado el programa:
	- $\mathtt{BE, FACTS, DRUL, HEADS, BODY, ARGLVL, LVL, DEFT, HEIGHT}$.
- El valor de sus métricas:
	- $\mathtt{NRU, NBE, NAR, NDT, ALE, AWI, AHE}$.
- El tiempo promedio para responder el estado de todos los literales del programa: $\mathtt{Time}$.

El mismo contiene los datos de **32000** programas. También es importante remarcar que se tiene acceso a los programas generados en sí, es decir, al conjunto de reglas que lo componen, esto nos permitiría hacer un análisis sintáctico de la estructura de cada regla en busca de algún patrón que nos permita predecir la complejidad del programa sin computar sus métricas.

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
