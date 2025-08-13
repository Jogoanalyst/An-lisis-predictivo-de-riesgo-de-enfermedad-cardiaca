🩺 Análisis Predictivo del Riesgo de Enfermedad Coronaria
Un proyecto de análisis de datos que utiliza técnicas de machine learning para predecir el riesgo de enfermedad coronaria en pacientes.

1. Descripción del Proyecto
Este repositorio contiene un análisis de datos exhaustivo para predecir si un paciente desarrollará una enfermedad coronaria en un plazo de 10 años. El proyecto aborda el desequilibrio de clases en los datos utilizando la técnica SMOTE, lo que resulta en un modelo de regresión logística más robusto y clínicamente relevante.

2. Objetivos
El objetivo principal de este análisis es:

Identificar los principales factores de riesgo asociados con las enfermedades coronarias.

Construir un modelo de clasificación binaria que pueda predecir con precisión el riesgo de la enfermedad.

Evaluar el rendimiento del modelo, prestando especial atención a su capacidad para identificar correctamente a los pacientes en la categoría de riesgo (clase positiva).

3. Fuentes de Datos
El conjunto de datos utilizado en este análisis proviene del famoso Estudio de Framingham, una de las investigaciones más importantes en la historia de la epidemiología cardiovascular. Los datos incluyen variables demográficas, de comportamiento y médicas de los pacientes.

4. Metodología
El análisis se llevó a cabo siguiendo un flujo de trabajo estándar en ciencia de datos:

Exploración y Preparación de Datos (EDA): Se realizó una limpieza de datos, incluyendo el tratamiento de valores atípicos, y se visualizaron las relaciones entre variables a través de mapas de calor y gráficos de quintiles.

Modelado Predictivo Inicial: Se construyó un modelo de Regresión Logística, el cual demostró una alta exactitud general pero un bajo rendimiento en la detección de la clase minoritaria (pacientes en riesgo).

Corrección de Desequilibrio de Clases: Se aplicó la técnica SMOTE para balancear el conjunto de datos de entrenamiento, mejorando así la capacidad del modelo para aprender de los casos positivos.

Evaluación Final del Modelo: Se evaluó el modelo mejorado,ificando su superioridad con métricas como el recall y el F1-score en la clase positiva.

5. Resultados y Conclusiones
Factores de Riesgo: El análisis confirmó que la edad, la presión sistólica (sysBP) y el colesterol total (totChol) son los factores de riesgo más influyentes.

Rendimiento del Modelo: El modelo final, ajustado con SMOTE, logró un recall del 63% en la clase positiva, un aumento significativo con respecto al 4% del modelo original. Aunque la exactitud general disminuyó, el modelo ahora es una herramienta mucho más valiosa para identificar a los pacientes que realmente necesitan atención.

Recomendación: Se sugiere utilizar este modelo para la detección temprana de pacientes con alto riesgo, permitiendo intervenciones médicas proactivas.

6. Tecnologías Utilizadas
Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Imblearn

7. Cómo Ejecutar el Proyecto
Clonar este repositorio.

Instalar las librerías necesarias ejecutando pip install -r requirements.txt. (Puedes generar este archivo con pip freeze > requirements.txt).

Abrir y ejecutar el notebook Analisis_predictivo_enfermedades_coronarias.ipynb.

Autor: Jonathan González

8. Diccionario de Variables
A continuación, se detalla el significado de las principales variables utilizadas en el análisis:

Variable	                Descripción
sex                         Género del paciente: M (masculino) o F (femenino).
age	                        Edad del paciente.
education               	Nivel de educación formal del paciente.
currentSmoker           	Indica si el paciente es fumador actual (Yes o No).
cigsPerDay	                Número de cigarrillos fumados por día.
BPMeds	                    Si el paciente toma medicación para la presión arterial (1=Sí, 0=No).
prevalentStroke	            Si el paciente ha tenido un accidente cerebrovascular previo (1=Sí, 0=No).
prevalentHyp	            Si el paciente tiene hipertensión (1=Sí, 0=No).
diabetes	                Si el paciente tiene diabetes (1=Sí, 0=No).
totChol	                    Nivel de colesterol total en mg/dL.
sysBP	                    Presión arterial sistólica.
diaBP	                    Presión arterial diastólica.
BMI                       	Índice de Masa Corporal.
heartRate               	Frecuencia cardíaca en latidos por minuto.
glucose                 	Nivel de glucosa en sangre.
TenYearCHD	                Variable objetivo: Indica si el paciente desarrolló una enfermedad coronaria en 10 años (1=Sí, 0=No).