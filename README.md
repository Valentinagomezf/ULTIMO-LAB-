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

## PARTE A
### 1. Fundamento teórico 
#### Actividad Simpática y Parasimpática del Sistema Nervioso Autónomo

El sistema nervioso autónomo regula las funciones involuntarias del cuerpo, incluyendo la función cardíaca, a través de dos ramas principales: el sistema simpático y el sistema parasimpático
Actividad Simpática: Generalmente asociada con respuestas de "lucha o huida", aumenta ante el estrés mental y cambios posturales (como pasar de estar acostado a estar de pie)
Actividad Parasimpática: Domina en estados de reposo, siendo su tono máximo cuando el sujeto se encuentra en posición supina (acostado boca arriba)

#### Efecto de la actividad simpática y parasimpática en la frecuencia cardíaca
Ambos sistemas ejercen un control antagónico sobre el nodo sinoauricular para regular el ritmo cardíaco
La estimulación simpática tiende a incrementar la frecuencia cardíaca (taquicardia) y es un marcador de la interacción simpato-vagal durante el estrés.
La estimulación parasimpática reduce la frecuencia cardíaca y es responsable de las variaciones rápidas latido a latido. El balance entre estas dos ramas produce fluctuaciones constantes en los intervalos entre latidos.

#### Variabilidad de la Frecuencia Cardíaca (HRV) a partir de un ECG

La HRV se define como la fluctuación de los intervalos R-R (el tiempo entre ondas R sucesivas en un electrocardiograma)
Medición: Se obtiene disparando la detección de la onda R en una señal de ECG, usualmente de una derivación estándar como la II, con una alta frecuencia de muestreo para garantizar precisión (ej. 2000 Hz)
Análisis convencional: Históricamente se han usado métodos como la desviación estándar (SD) y el análisis espectral. El análisis espectral divide la variabilidad en componentes de alta frecuencia (HF), que reflejan exclusivamente el tono vagal, y de baja frecuencia (LF), que reflejan tanto el tono simpático como el vagal.

#### Diagrama de Poincaré como herramienta de análisis de la serie R-R

El Diagrama de Poincaré o Poincaré Plot en inglés es una herramienta no lineal ampliamente utilizada para analizar la serie de intervalos R-R y caracterizar la HRV. Su construcción es relativamente sencilla y requiere haber definido previamente la lista de los tiempos (en ms) en los que se detectaron los R-R:








  
## PARTE C 
En esta etapa se construyeron los diagramas de Poincaré a partir de los intervalos R-R obtenidos de la señal ECG, permitiendo analizar la dispersión y el comportamiento dinámico de la frecuencia cardíaca durante las condiciones de reposo y lectura en voz alta. Además, se implementó la elipse de dispersión para calcular los parámetros SD1 y SD2 asociados a la variabilidad cardíaca.

Finalmente, se calcularon los índices CSI y CVI con el fin de evaluar la actividad simpática y parasimpática del sistema nervioso autónomo, comparando los cambios fisiológicos presentes en cada segmento de la señal.
### DIAGRAMA 
