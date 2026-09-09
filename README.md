# Trabajo Práctico Final - Inteligencia Artificial (2nd Cuatrimestre 2026)
**Universidad Nacional Guillermo Brown (UNAB)**
* **Docente:** Pablo Moreira
* **Integrantes - Grupo 1:** Pablo Calvo, Cristian Alias, Eduardo Morales
* **Dataset asignado:** Plant Village (Updated) - 70,000 imágenes de hojas de plantas sanas y enfermas (9 especies).

---

## 🎯 1. Introducción y Objetivo General
El objetivo de este trabajo práctico es construir, paso a paso, un sistema de Machine Learning que evolucione desde un modelo *baseline* hasta una arquitectura compleja, aplicando los conceptos teóricos y prácticos de cada unidad de la materia. No se busca solo que el modelo funcione, sino poder justificar cada decisión de diseño, interpretar resultados y aplicar técnicas de mejora de manera sistemática.

---

## 📈 2. Estructura y Etapas del Proyecto
El desarrollo se organiza de forma progresiva a lo largo de las siguientes secciones en el Notebook Jupyter:

* **Etapa 1 - Exploración y Modelo Baseline (Obligatorio):**
  * Análisis Exploratorio de Datos (EDA), tipos de variables, distribuciones y detección de problemas (desbalance, outliers).
  * Partición de datos en Entrenamiento, Desarrollo (Dev) y Prueba (Test) con justificación de la estrategia estratificada.
  * Preprocesamiento mínimo y establecimiento del modelo *baseline* (red densa simple) con métrica de evaluación de número único (*Accuracy* / *F1-Macro*).
* **Etapa 2 - Red Neuronal Multicapa y Análisis de Errores (Obligatorio):**
  * Análisis de errores manual sobre una muestra de ejemplos mal clasificados en el conjunto Dev (sesgo, varianza, data mismatch).
  * Diseño e implementación de una red neuronal densa (MLP) con al menos 3 capas ocultas.
  * Aplicación de técnicas de regularización (Dropout, L2, Batch Normalization, Early Stopping) y comparación de curvas de aprendizaje.
* **Etapa 3 - Arquitectura Específica de Dominio (Obligatorio - Enfoque de Imágenes):**
  * Implementación de una Red Convolucional (CNN) con al menos 3 bloques convolucionales (`Conv2D` + `ReLU` + `MaxPooling`).
  * Comparación de enfoque *End-to-End* versus pipeline secuencial (extractor de features + clasificador).
  * Aplicación de *Data Augmentation* (flip, rotación, zoom) y atribución de errores.
* **Etapa 4 - Modelo Generativo: VAE o DCGAN (Optativo):**
  * Elección, justificación y diseño de un modelo generativo sobre el espacio latente.
  * Entrenamiento, visualización de pérdidas, interpolación y análisis de calidad de muestras generadas.
* **Etapa 5 - Cierre, Comparación y Análisis Ético (Obligatorio):**
  * Tabla comparativa integral de todos los modelos desarrollados (parámetros, métricas en Dev/Test, tiempos).
  * Evaluación final en el conjunto Test (por primera y única vez) y análisis de *overfitting*.
  * Análisis ético, de sesgos del dataset por subgrupos y reflexión sobre el impacto en sistemas reales.
  * Conclusiones finales, aprendizajes y limitaciones.

---

## 🛠️ 3. Instrucciones para Reproducir el Entorno
1. **Entorno recomendado:** Google Colab (con acceso a GPU T4 para agilizar las etapas convolucionales).
2. **Stack tecnológico:** Python 3.10+, TensorFlow / Keras 2.x, scikit-learn, matplotlib / seaborn.
3. **Ejecución:** Clonar o descargar el repositorio, abrir el notebook principal (`.ipynb`) en Google Colab y ejecutar las celdas en orden secuencial. La primera celda incluye la descarga automatizada del dataset de Kaggle.

---

## 📂 4. Estructura de la Carpeta de Entrega
```text
TP_IA2026_PlantVillage/
│
├── notebook.ipynb         # Cuaderno principal comentado paso a paso
├── requirements.txt       # Librerías necesarias y versiones
├── README.md              # Instrucciones del proyecto y entorno
└── resultados/            # Carpeta con gráficos y métricas exportadas
