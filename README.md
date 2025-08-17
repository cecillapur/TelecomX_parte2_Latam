# Challenge Data Science LATAM - Parte 2: Predicción de Cancelación de Clientes (Churn)

## Descripción General
Este proyecto aborda el análisis y modelado predictivo de la cancelación de clientes (churn) en una empresa de telecomunicaciones. Se parte de un dataset tratado en la Parte 1 y se desarrolla un pipeline completo de análisis exploratorio, preprocesamiento, modelado y recomendaciones de negocio.

## Pasos Realizados

### 1. Carga y limpieza de datos
- Se cargó el archivo `datos_tratados.csv` generado en la Parte 1.
- Se eliminaron columnas irrelevantes como identificadores únicos.
- Se revisó la estructura y tipos de datos.

### 2. Preprocesamiento
- Se aplicó codificación one-hot a variables categóricas.
- Se imputaron valores faltantes (media para numéricos, moda para categóricos).
- Se normalizaron las variables numéricas con StandardScaler.
- Se aseguró que la variable objetivo `Churn` fuera numérica.

### 3. Análisis exploratorio
- Se verificó el balance de clases de la variable `Churn`.
- Se visualizó la matriz de correlación y la relación de variables con la cancelación.
- Se realizaron boxplots y scatterplots para investigar relaciones clave.

### 4. Balanceo de clases
- Se aplicó SMOTE para balancear la clase minoritaria en el set de entrenamiento (opcional).

### 5. División de datos
- Se dividieron los datos en conjuntos de entrenamiento y prueba (80/20), estratificando por la variable objetivo.

### 6. Modelado
- Se entrenaron y evaluaron los siguientes modelos:
  - **Regresión Logística** (con normalización)
  - **Random Forest** (sin normalización)
  - **KNN** (K-Nearest Neighbors)
  - **SVM** (Support Vector Machine, kernel lineal)
- Se calcularon métricas: exactitud, precisión, recall, F1-score y matriz de confusión para cada modelo.

### 7. Importancia de variables
- Se analizaron los coeficientes de Regresión Logística y SVM.
- Se graficó la importancia de variables en Random Forest y KNN (por permutación).

### 8. Conclusiones y recomendaciones
- Se identificaron los principales factores que influyen en la cancelación: antigüedad, gastos, tipo de contrato, servicios adicionales y método de pago.
- Se propusieron estrategias de retención basadas en los resultados de los modelos.

## Recomendaciones de negocio
- Fidelizar clientes con poca antigüedad.
- Revisar y ajustar tarifas y cargos.
- Promover contratos a largo plazo.
- Mejorar servicios adicionales y soporte.
- Optimizar métodos de pago.

## Cómo ejecutar el análisis
1. Asegúrate de tener los archivos `datos_tratados.csv` y el notebook `TelecomX_2_LATAM.ipynb` en la misma carpeta.
2. Instala las dependencias necesarias (ver `requirements.txt`).
3. Abre y ejecuta el notebook en Jupyter o VS Code.

## Dependencias principales
- pandas
- numpy
- scikit-learn
- imbalanced-learn
- matplotlib
- seaborn

---

**Autor:** Equipo Data Science LATAM

**Fecha:** Agosto 2025
