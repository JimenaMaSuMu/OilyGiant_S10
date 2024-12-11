# OilyGiant_S10
OilyGiant: Selección de Regiones para el Desarrollo de Pozos Petrolíferos
Descripción del Proyecto
En OilyGiant, buscamos identificar las mejores ubicaciones para desarrollar 200 nuevos pozos petrolíferos con el objetivo de maximizar el beneficio total mientras minimizamos los riesgos. Este proyecto se enfoca en utilizar modelos de regresión lineal para predecir el volumen de reservas y seleccionar la región con el mayor margen de beneficio cumpliendo con las condiciones del negocio.

Objetivos del Proyecto
Crear un modelo predictivo:
Predecir el volumen de reservas en nuevos pozos petrolíferos utilizando datos de exploración geológica de tres regiones.
Selección de pozos petrolíferos:
Elegir los 200 pozos con las reservas estimadas más altas en cada región.
Evaluación de beneficios:
Calcular las ganancias potenciales y analizar los riesgos utilizando la técnica de bootstrapping.
Recomendación final:
Proponer la mejor región para desarrollar pozos, justificando la elección basada en análisis de beneficios y riesgos.
Descripción de los Datos
Los datos geológicos de las tres regiones están disponibles en los siguientes archivos CSV:

geo_data_0.csv
geo_data_1.csv
geo_data_2.csv

Columnas:
id: Identificador único del pozo.
f0, f1, f2: Tres características geológicas (significado específico no relevante, pero significativas para el modelo).
product: Volumen de reservas en el pozo (en miles de barriles).

Metodología
1. Preparación de Datos
Carga y limpieza de los datos.
División del conjunto en entrenamiento y validación (75:25).
Preprocesamiento para garantizar que los datos sean adecuados para la regresión.
2. Modelado Predictivo
Entrenamiento de un modelo de regresión lineal en cada región.
Evaluación del modelo usando:
Volumen promedio predicho de reservas.
Raíz del Error Cuadrático Medio (RMSE).

3. Selección de Pozos
Selección de los 200 pozos con los valores de predicción más altos en cada región.
Cálculo de ganancias basado en:
Presupuesto total: $100 millones para desarrollar 200 pozos.
Ingresos por unidad: $4,500 por cada mil barriles.
4. Análisis de Beneficios y Riesgos
Uso de bootstrapping (1000 iteraciones) para calcular:
Beneficio promedio.
Intervalo de confianza del 95%.
Riesgo de pérdidas (probabilidad de obtener una ganancia negativa).

5. Recomendación Final
Comparación de regiones con base en:
Beneficio promedio más alto.
Riesgo de pérdidas menor al 2.5%.
Resultados Esperados
Modelos de regresión lineal para las tres regiones con métricas de desempeño claras (RMSE).
Análisis comparativo de las tres regiones en términos de:
Beneficio potencial.
Riesgo de pérdidas.
Recomendación justificada de la región óptima para el desarrollo de pozos.
Requisitos del Sistema
Lenguaje: Python
Librerías:
Pandas, NumPy (manipulación y análisis de datos).
Scikit-learn (modelado de regresión).
Matplotlib, Seaborn (visualización de datos).
SciPy (implementación de bootstrapping).