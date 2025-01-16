# Análisis Predictivo de Salarios y Contratación en el Sector Tecnológico

## Introducción 

Este proyecto se enfoca en el análisis de datos de recursos humanos para predecir el salario de los postulantes y determinar si serán contratados, basándose en diferentes factores. Este análisis se realiza utilizando técnicas de modelado de datos para entender mejor las tendencias del mercado laboral en el sector tecnológico.

## Contexto 

Un equipo de Recursos Humanos proporcionó datos que incluyen características de los postulantes que consideran influyentes en el salario que buscan, así como información sobre si fueron o no contratados. El objetivo es crear modelos predictivos que ayuden a la empresa a tomar decisiones más informadas en la contratación. Los datos incluyen información como:
•	Experiencia: Años de experiencia en el área.
•	Posición: Cargo al que aspira el postulante (Analista, Coordinador, Gerente).
•	Hijos: Número de hijos del postulante.
•	Casado: Estado civil del postulante (0 para no casado, 1 para casado).
•	Educación: Nivel máximo de estudios del postulante (Bachillerato, Licenciatura, Posgrado).
•	Salario: Cantidad en pesos mexicanos que el postulante solicita como salario.
•	Contratado: Indica si el postulante fue contratado (0 para no contratado, 1 para contratado).

## Objetivo El proyecto tiene dos objetivos principales:

•	Predicción Salarial: Desarrollar un modelo de regresión lineal para predecir el salario que un postulante solicitará, basándose en sus características.
•	Clasificación de Contratación: Crear un modelo de regresión logística para predecir si un postulante será contratado o no.

## Conjunto de datos 

Se utilizaron dos conjuntos de datos, ambos con 1000 registros, que contienen información de postulantes a empresas de tecnología. Ambos conjuntos de datos incluyen las siguientes columnas: Experiencia, Posicion, Hijos, Casado, Educacion, Salario. El segundo conjunto de datos también incluye una columna adicional llamada Contratado.

•	Los datos se cargaron usando la librería Pandas.
•	Se exploraron y limpiaron los datos, verificando valores únicos, nulos y duplicados, asegurando la calidad de los datos para el modelado.
•	Se eliminaron valores atípicos para mejorar el rendimiento del modelo.
•	Se convirtieron las variables categóricas a numéricas mediante codificación one-hot, creando columnas dummy para cada categoría.

## Metodología Para alcanzar los objetivos, se emplearon las siguientes metodologías:

•	Preprocesamiento de datos: Se realizó una limpieza exhaustiva de los datos, tratamiento de valores faltantes y codificación de variables categóricas para preparar los datos para el modelado.
•	Modelado: 
o	Regresión Lineal: Se utilizó para predecir el salario de los postulantes basándose en sus características.
o	Regresión Logística: Se empleó para clasificar si un postulante sería contratado o no.
o	Máquinas de Vectores de Soporte (SVM): Se implementó como modelo de clasificación adicional para comparar el rendimiento con la regresión logística.
•	Evaluación: Se utilizaron métricas como el Error Cuadrático Medio (MSE), la Raíz del Error Cuadrático Medio (RMSE) y el Coeficiente de Determinación (R2) para evaluar el modelo de regresión lineal. Para los modelos de clasificación, se utilizaron la matriz de confusión, la precisión (accuracy) y el Área Bajo la Curva ROC (AUC).
•	División de datos: Los datos se dividieron en conjuntos de entrenamiento (80%) y prueba (20%) para entrenar los modelos y evaluar su rendimiento.
•	Estandarización de variables: Se estandarizaron las variables independientes para mejorar el rendimiento del modelo.

## Resultados

•	Modelo de Regresión Lineal: Se logró un modelo que predice el salario de los postulantes con un R2 de 0.70, lo que indica que el modelo explica el 70% de la variabilidad del salario. El RMSE fue de 6494.37, lo que significa que, en promedio, las predicciones del modelo tienen una desviación de alrededor de 6494.37 pesos mexicanos. La ecuación de la regresión lineal fue: Salario = 16352.36118404 + 2956.319595 * Experiencia + 1717.266785 * Hijos + ....
•	Modelo de Regresión Logística: El modelo de regresión logística tuvo una precisión del 70% en la predicción de si un postulante sería contratado o no. El área bajo la curva ROC (AUC) fue de 0.6675, lo que indica una capacidad discriminativa moderada del modelo.
•	Modelo SVM: El modelo SVM obtuvo una precisión del 74%.

## Conclusiones

•	Los modelos desarrollados muestran un buen desempeño en la predicción de salarios y en la clasificación de la contratación de postulantes.
•	La experiencia es una variable clave para predecir el salario, ya que existe una relación lineal positiva entre ambas.
•	El modelo de regresión lineal es capaz de explicar un porcentaje significativo de la variabilidad en los salarios, sin embargo, hay variabilidad no explicada por el modelo.
•	El modelo de regresión logística muestra una capacidad moderada para discriminar entre los postulantes contratados y no contratados.
•	El modelo SVM resultó ligeramente más preciso que el modelo de regresión logística para predecir si un postulante será contratado.

## Herramientas

•	Python: Lenguaje de programación principal para el desarrollo del proyecto.
•	Pandas: Para manipulación y análisis de datos.
•	NumPy: Para operaciones numéricas.
•	Scikit-learn: Para la implementación de modelos de machine learning (regresión lineal, regresión logística y SVM), así como métricas de evaluación.
•	Matplotlib y Seaborn: Para visualización de datos.

