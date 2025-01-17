# Análisis Predictivo de Salarios y Contratación en el Sector Tecnológico

## Introducción

Este proyecto se centra en el análisis de datos de recursos humanos para predecir el salario de los postulantes y determinar si serán contratados, utilizando técnicas de modelado de datos. El objetivo es entender mejor las tendencias del mercado laboral en el sector tecnológico y apoyar la toma de decisiones informadas en procesos de contratación.

---

## Contexto

Un equipo de Recursos Humanos proporcionó datos que incluyen diversas características de los postulantes influyentes en:

1. El salario solicitado por los postulantes.
2. La decisión de contratación por parte de la empresa.

### Características de los datos

- **Experiencia**: Años de experiencia en el área.
- **Posición**: Cargo deseado (Analista, Coordinador, Gerente).
- **Hijos**: Número de hijos del postulante.
- **Casado**: Estado civil (0 para no casado, 1 para casado).
- **Educación**: Nivel máximo de estudios (Bachillerato, Licenciatura, Posgrado).
- **Salario**: Cantidad solicitada en pesos mexicanos.
- **Contratado**: Indica si el postulante fue contratado (0 para no contratado, 1 para contratado).

---

## Objetivos

1. **Predicción Salarial**: Desarrollar un modelo de regresión lineal para estimar el salario solicitado.
2. **Clasificación de Contratación**: Crear modelos predictivos para determinar si un postulante será contratado.

---

## Conjunto de Datos

Dos conjuntos de datos, cada uno con 1000 registros, fueron utilizados. Contienen las siguientes columnas comunes:

- Experiencia
- Posición
- Hijos
- Casado
- Educación
- Salario

El segundo conjunto incluye además la columna "Contratado".

### Procesamiento de los datos:

- Carga de datos con la librería **Pandas**.
- Exploración y limpieza de datos:
  - Verificación de valores únicos, nulos y duplicados.
  - Eliminación de valores atípicos.
- Transformación de variables categóricas en numéricas mediante **one-hot encoding**.

---

## Metodología

1. **Preprocesamiento de Datos**:
   - Limpieza y tratamiento de valores faltantes.
   - Codificación de variables categóricas.
   - Estandarización de variables independientes para mejorar el rendimiento de los modelos.

2. **Modelado**:
   - **Regresión Lineal**: Predicción de salario.
   - **Regresión Logística**: Clasificación de postulantes contratados.
   - **SVM (Support Vector Machines)**: Modelo adicional para comparar el rendimiento con la regresión logística.

3. **Evaluación de Modelos**:
   - **Regresión Lineal**:
     - Error Cuadrático Medio (MSE).
     - Raíz del Error Cuadrático Medio (RMSE).
     - Coeficiente de Determinación (R2).
   - **Modelos de Clasificación**:
     - Precisión (accuracy).
     - Matriz de confusión.
     - Área Bajo la Curva ROC (AUC).

4. **División de Datos**:
   - 80% para entrenamiento.
   - 20% para prueba.

---

## Resultados

1. **Modelo de Regresión Lineal**:
   - **R2**: 0.70 (70% de la variabilidad del salario explicada).
   - **RMSE**: 6494.37 MXN (desviación promedio de las predicciones).
   - **Ecuación del modelo**:
     ```
     Salario = 16352.361 + 2956.319 * Experiencia + 1717.267 * Hijos + ...
     ```

2. **Modelo de Regresión Logística**:
   - **Precisión**: 70%.
   - **AUC**: 0.6675 (capacidad discriminativa moderada).

3. **Modelo SVM**:
   - **Precisión**: 74% (mejor rendimiento comparado con la regresión logística).

---

## Conclusiones

- **Predicción Salarial**: El modelo de regresión lineal explica una proporción significativa de la variabilidad del salario, pero hay factores adicionales que podrían mejorar la predicción.
- **Clasificación de Contratación**: Los modelos de regresión logística y SVM tienen un buen rendimiento, con SVM mostrando una ligera ventaja.
- **Variable Clave**: La experiencia es un factor determinante tanto en la predicción de salarios como en la contratación.

---

## Herramientas

- **Python**: Lenguaje principal.
- **Pandas**: Manipulación y análisis de datos.
- **NumPy**: Operaciones numéricas.
- **Scikit-learn**: Implementación de modelos de machine learning y métricas de evaluación.
- **Matplotlib y Seaborn**: Visualización de datos.

---

Este proyecto demuestra la aplicación de técnicas de ciencia de datos en el análisis predictivo, brindando valiosas herramientas para optimizar procesos de contratación en el sector tecnológico.
