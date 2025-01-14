# Datos para la inclusión: Análisis de las dinámicas crediticias de FINAGRO (2021-2024) en la inclusión financiera, diversificación agropecuaria y equidad de género en zonas rurales y de posconflicto en Colombia

## Resumen

Investigación fundamentada en el proceso de análisis exploratorio de datos, y presentación visual de "insights" y KPIs de un historial de operaciones crediticias llevadas a cabo por el Fondo para el Financiamiento del Sector Agropecuario (FINAGRO) entre enero de 2021 y septiembre de 2024, y puestas a disponibilidad pública en el Portal de Datos Abiertos Nacional de Colombia, en el que se busca entender el impacto de los créditos colocados sobre tres dimensiones de estudio: 1) inclusión financiera, 2) diversificación agropecuaria y 3) equidad de género. Los resultados del análisis arrojaron que FINAGRO ha diversificado la agricultura y contribuido a la modernización del sector rural con tecnologías sostenibles y cultivos no tradicionales, reduciendo la dependencia de monocultivos, aunque los créditos colocados para este destino son muy bajos. Por otro lado, la  entidad ha impulsado significativamente la autonomía económica de mujeres rurales, superando el 35% en créditos asignados a este grupo en comparación con el total de colocaciones. Además, la ejecución de planes de créditos especiales han permitido en las zonas de post-conflicto, la generación de empleo, la inversión en infraestructura y cohesión social, aunque los créditos en estas regiones han disminuido desde 2021.

## Entendimiento de la problemática del negocio
Los directivos de una empresa industrial, dedicada al desarrollo de tecnología automotríz, estan interesados en construir un modelo estadístico que permite predecir cuando un empleado abandona la empresa o no, a partir de algunos indicadores y datos que ha recodigo el área de Talento Humano para cada trabajador activo o retirado de la institución, con el objetivo de ejecutar acciones preventivas que minimicen la deserción del talento. Este interés surgió como respuesta a los resultados de una investigación interna que concluyó que el incremento en los costos operativos experimentados en los últimos 6 años se originaron por la necesidad de entrenamiento de nuevos empleados, perdidas materiales en el área como consecuencia de una baja adaptabilidad a los procedimientos operativos y la poca eficiencia de los procesos.

## Entendimiento de los datos
El conjunto de datos aportados por la empresa industrial está comprendido por 14999 registros únicos e independientes y 10 características. Las características o variables incluyen información sobre el nivel de satisfacción comunicado por el trabajador, el nivel de desempeño calculado por el área al que pertenece, el número de proyectos en los que ha participado el trabajador, el promedio de horas mensuales trabajadas, la antigüedad del empleado, las promociones de cargo, el nivel salarial, el área o departamento al que pertenece, si ha sufrido accidentes laborales y si se el trabajador se encuentra activo o retirado de la empresa.
El gráfico a continuación muestra  la distribución de cuantos empleados activos y retirados existen en el conjunto de datos.

<img src="assets/img/img1.png" alt="Distribución de datos" style="display: block; margin: auto; max-width: 30%; height: auto;">

Como parte de la preparación para modelado de los datos, se eliminaron columnas innecesarias, se verificaron valores nulos y registros duplicados, se gestionaron valores atípicos y se formatearon en el tipo de datos adecuado.

## Modelado y Evaluación

Se seleccionó un modelo de potenciación de grádiente extremo (XGBoost) como mejor opción, compuesto por 500 árboles de decisión para determinar la importancia de las características sobre qué empleado desertaría de su cargo o no. El gráfico a continuación muestra que el tiempo en la empresa (antigüedad), el nivel de satisfacción comunicado (satisfaccion) y la cantidad de proyectos en los que ha participado (numero_proyectos) fueron los tres factores más importantes para determinar si un trabajador abandonaría la empresa. El modelo en general tuvo un rendimiento general del 98,8%, 96,5% de sensibilidad y una capacidad de discriminación del 98%, lo que quiere decir que fue capaz de discriminar y clasificar correctamente casi la totalidad de casos en el conjunto de datos de prueba, mientras identificó con alta efectividad a los empleados en riesgo de retirarse, con un 96,5% de certeza.

El gráfico de barras horizontal muestra la importancia de las características del modelo XGBoost.

<img src="assets/img/img2.png" alt="Distribución de datos" style="display: block; margin: auto; max-width: 50%; height: auto;">

## Conclusión

Este modelo puede ayudar a la empresa a mejorar la retención de talento humano, permitiendo realizar predecciones sobre qué empleados están en riesgo de abandonar la empresa, convirtiendose en una base decisiva para la elaboración de un plan de acciones preventivas mientras se abordar las causas subyacentes de la deserción del talento. 
En escenarios fúturos de investigación se recomienda recolectar y adicionar información sobre el tipo de retiro (voluntario o causal), la posición jerárquica del cargo del empleado, la edad, la cantidad de quejas o solicitudes, la modalidad de trabajo y la jornada laboral. Estos datos adicionales podrían generar un mayor entendimiento de la dinámica de deserción.
