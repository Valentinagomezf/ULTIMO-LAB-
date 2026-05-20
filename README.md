# LAB 5 
# Variabilidad de la Frecuencia Cardíaca (HRV) y balance autonómico 
## DESCRIPCIÓN 
Esta práctica tuvo como objetivo analizar la variabilidad de la frecuencia cardíaca (HRV) a partir de señales electrocardiográficas (ECG), con el fin de identificar cambios en el balance autonómico del sistema nervioso simpático y parasimpático. Para ello, se adquirió una señal ECG durante dos condiciones experimentales diferentes: reposo y lectura en voz alta.
Posteriormente, la señal fue sometida a un proceso de preprocesamiento mediante filtros digitales IIR para reducir el ruido e interferencias presentes durante la adquisición. Después del filtrado, se realizó la detección de los picos R y el cálculo de los intervalos R-R, permitiendo obtener métricas de HRV en el dominio del tiempo, como la media y la desviación estándar de los intervalos cardíacos.

Finalmente, se construyeron diagramas de Poincaré para cada segmento de la señal, permitiendo evaluar el comportamiento autonómico mediante los índices de actividad vagal (CVI) y actividad simpática (CSI). El análisis comparativo permitió evidenciar las variaciones fisiológicas producidas por las diferentes condiciones de adquisición.
## OBJETIVOS 
- Adquirir señales electrocardiográficas bajo condiciones de reposo y actividad verbal controlada.
- Diseñar e implementar filtros digitales IIR para el preprocesamiento de la señal ECG.
- Detectar los picos R y calcular los intervalos R-R de la señal cardíaca.
- Analizar parámetros de HRV en el dominio del tiempo, como la media y la desviación estándar de los intervalos R-R.
- Construir y analizar diagramas de Poincaré para evaluar la actividad simpática y parasimpática.
- Comparar los cambios fisiológicos observados entre las diferentes condiciones experimentales.
## PARTE C 
En esta etapa se construyeron los diagramas de Poincaré a partir de los intervalos R-R obtenidos de la señal ECG, permitiendo analizar la dispersión y el comportamiento dinámico de la frecuencia cardíaca durante las condiciones de reposo y lectura en voz alta. Además, se implementó la elipse de dispersión para calcular los parámetros SD1 y SD2 asociados a la variabilidad cardíaca.

Finalmente, se calcularon los índices CSI y CVI con el fin de evaluar la actividad simpática y parasimpática del sistema nervioso autónomo, comparando los cambios fisiológicos presentes en cada segmento de la señal.
### DIAGRAMA 
