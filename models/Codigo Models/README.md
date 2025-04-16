# Predicción de Apertura de Ventanas en la Próxima Hora

Este directorio contiene dos notebooks que trabajan en conjunto para predecir si las ventanas se abrirán en la próxima hora, utilizando sensores, variables meteorológicas y modelos de machine learning.

## 📘 Notebooks incluidos

### 1. `01_prediccion_temperatura.ipynb`
Este notebook carga un modelo previamente entrenado (`model_predict_temperaturas.keras`) para predecir la temperatura esperada en el futuro cercano, usando como entrada múltiples variables ambientales:

- Humedad, presión y temperatura de sensores
- Estado de la puerta y ventanas
- Azimut y elevación del sol
- Temperatura exterior y porcentaje de nubes
- Representación horaria (sin/cos), mes y estación
- Día de la semana

El resultado es una nueva columna en el dataset: `temperatura_predicha`.

### 2. `02_modelo_clasificacion_ventanas.ipynb`
Entrena un modelo de clasificación binaria que predice si las ventanas estarán abiertas durante la siguiente hora. Utiliza como entrada el dataset enriquecido con la `temperatura_predicha`.

El flujo incluye:
- Preprocesamiento del dataset
- División en sets de entrenamiento, validación y test
- Definición y entrenamiento de una red neuronal con Keras
- Evaluación mediante métricas: accuracy, precision, recall, F1 y MAE
- Visualización de métricas de entrenamiento (pérdida y MAE)

## 🔧 Tecnologías utilizadas

- Python 3
- TensorFlow / Keras
- pandas, NumPy, scikit-learn
- Matplotlib
- Google Colab (como entorno de ejecución)

## ▶️ Cómo ejecutar

1. Asegúrate de tener instaladas todas las dependencias necesarias:
   ```bash
   pip install tensorflow pandas numpy scikit-learn matplotlib
