# Predicción y Clasificación de Oportunidades de Venta

Este proyecto tiene como objetivo predecir y clasificar oportunidades de venta utilizando múltiples modelos supervisados de Machine Learning. Se realiza un análisis comparativo de los modelos y sus métricas de desempeño, además de una exploración de reducción de dimensionalidad para facilitar la visualización.

## Contenido del Proyecto

### 1. Introducción
- Contexto: Clasificación de oportunidades de ventas como "ganadas" o "perdidas".
- Objetivo: Seleccionar el modelo más óptimo en términos de precisión, recall, F1-score, y tiempo de ejecución.

### 2. Preprocesamiento de Datos
- **Transformación de Datos:** Codificación de variables categóricas con One-Hot Encoding.
- **Normalización:** Escalado de variables numéricas con MinMaxScaler.
- **Conjuntos de Entrenamiento y Prueba:** División estratificada para mantener la proporción entre clases.

### 3. Modelos de Machine Learning
Se implementan y comparan varios modelos supervisados:
1. **K-Nearest Neighbors (KNN):**
   - Análisis del error de generalización para diferentes valores de `k`.
   - Reporte de métricas: Precisión, Recall y F1-score.

2. **Árbol de Decisión:**
   - Optimización de hiperparámetros (`max_depth`, `min_samples_split`, etc.) usando Grid Search.
   - Evaluación del mejor modelo con métricas de desempeño.

3. **Support Vector Machine (SVM) con Kernel Gaussiano:**
   - Uso de reducción de dimensionalidad (PCA) para visualización y análisis del modelo.
   - Búsqueda de hiperparámetros óptimos (`C` y `gamma`).

4. **Random Forest (Bosque Aleatorio):**
   - Entrenamiento y ajuste de hiperparámetros.
   - Comparación con el Árbol de Decisión y análisis de métricas.

### 4. Reducción de Dimensionalidad
- **Análisis PCA:** Reducción a dos componentes principales para visualización.
- **Curva de Varianza Acumulada:** Selección del número óptimo de componentes principales.

### 5. Conclusión
- El modelo más eficiente y preciso para clasificar oportunidades de ventas es el Árbol de Decisión:
  - Alto F1-score para ambas clases.
  - Corto tiempo de ejecución en comparación con Random Forest y SVM.
- Los modelos Random Forest y SVM también son útiles, pero menos eficientes en términos de recursos y tiempo.

## Resultados
- **KNN:** Buen desempeño en clases mayoritarias, pero bajo en clases minoritarias.
- **Árbol de Decisión:** Modelo con mejor equilibrio entre precisión y eficiencia.
- **Random Forest:** Mejor generalización, pero menor F1-score para oportunidades ganadas.
- **SVM:** Buen desempeño, pero con tiempos de entrenamiento más largos.

## Referencias
1. **Keyrus:** Make Data Matter. [Enlace](https://keyrus.com/latam/es/home)
2. **UNAL:** Programa de Formación en Machine Learning and Data Science. [Enlace](https://ingenieria.bogota.unal.edu.co/uec/?p=10947)

## Licencia
Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo `LICENSE` para más detalles.
