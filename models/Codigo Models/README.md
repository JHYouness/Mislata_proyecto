Aquí tienes una versión mejorada y más completa del `README.md` para un trabajo serio de instituto, incluyendo los resultados de los modelos y mejorando la redacción para mayor claridad y formalidad:

---

# 📡 Predicción de Apertura de Ventanas en la Próxima Hora

Este directorio contiene los notebooks para entrenar a los modelos de predicción de apertura de ventanas en la siguiente hora. 

## 🪟 Estructura:

- <a href="https://github.com/JHYouness/Mislata_proyecto/tree/main/models/Codigo%20Models" target="_blank">`/Codigo Models`</a>: contiene el código fuente en Python utilizado para entrenar los modelos (`.ipynb`).
- <a href="https://github.com/JHYouness/Mislata_proyecto/tree/main/models" target="_blank">`../models`</a>: modelos entrenados exportados en formato Keras para su reutilización y despliegue.

## 📘 Notebooks incluidos

### 1. `modelo_temperatura.ipynb`

Este notebook entrena un modelo para predecir la temperatura futura en la siguiente hora. Se genera la columna `temperatura_predicha`, que posteriormente se usa como entrada en el modelo final.

#### **Variables de entrada:**

- Humedad, presión y temperatura de sensores
- Estado de puertas y ventanas
- Posición solar (azimut y elevación)
- Temperatura exterior y porcentaje de nubosidad
- Hora del día (representación circular: seno y coseno)
- Mes y estación del año
- Día de la semana

#### **Resultados del modelo:**

Configuración: Dataset no filtrado (incluye horas nocturnas y findes).

- `loss`: **0.0998**
- `mae`: **0.2517**
- `val_loss`: **0.2286**
- `val_mae`: **0.3744**

---

### 2. `modelo_final.ipynb`

Este notebook entrena un modelo de clasificación binaria con el objetivo de predecir si las ventanas estarán abiertas durante la próxima hora. Utiliza como entrada el dataset pero carga y reutiliza un modelo previamente entrenado (`model_predict_temperaturas.keras`) para generar la característica `temperatura_predicha`.

#### **Resultados del modelo final:**

- `activation`: **ReLU**
- `optimizer`: **Adam**
- `learning_rate`: **0.001**
- `accuracy`: **0.967**
- `precision`: **0.974**
- `recall`: **0.950**

---

## 🔧 Tecnologías utilizadas

- Python 3
- TensorFlow / Keras
- pandas, NumPy, scikit-learn
- Matplotlib
- Google Colab / Jupyter lab y Miniconda (como entorno de desarrollo y entrenamiento)
