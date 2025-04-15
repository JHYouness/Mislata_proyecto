# 📦 Codigo Models

Este directorio contiene los archivos relacionados con el entrenamiento y evaluación de modelos. Aquí es donde se lleva a cabo la fase de *modelado* tras la limpieza de los datos.

---

## 📘 Notebooks

### 🔹 `modelo_final.ipynb`

Notebook principal que entrena y guarda el modelo que predice si la puerta va a ser abierta en la siguiente hora.  
- Usa los datos procesados de la capa *gold* y los limpia ligeramente para que se adapten al problema (limita de 7:00 a 21:00).  
- Guarda los modelos resultantes en formato `.keras`.  
- Evalúa varias redes neuronales y elegimos en función de las métricas.
- Normaliza los datos

### 🔹 `modelo_temperatura.ipynb`

Notebook enfocado en clasificación binaria: predice si un estado es *abierto* o *cerrado* según sensores y condiciones.  
- Usa los datos procesados de la capa *gold* y los limpia ligeramente para que se adapten al problema (limita de 7:00 a 21:00).  
- Guarda los modelos resultantes en formato `.keras`.  
- Normaliza los datos

---

## 🧠 Modelos Exportados

Los modelos entrenados se guardan en este directorio con el siguiente nombre:

- `model_predicciones_se_abrira.keras`: modelo que predice si la puerta va a ser abierta en la siguiente hora.
- `model_predict_temperaturas.keras`: modelo de regresión para predicción de temperatura en la sala que determina si la calefacción se encenderá.

---

## 📁 Estructura del proyecto

```bash
├── Codigo Models/
│   ├── modelo_final.ipynb             # Entrenamiento de modelo final
│   └──  modelo_temperatura.ipynb             # Entrenamiento de primer modelo
├── model_predicciones_se_abrira.keras          # Modelo final exportado (clasificación)
├── model_predict_temperaturas.keras            # Modelo predicción temperatura exportado (regresión)
└── readme.md                                   # Este archivo
```

---

## Notas

- Los modelos están pensados para integrarse directamente con los pipelines definidos en `airflow/`.  
--- 

