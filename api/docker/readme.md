# 🌡️ Proyecto Sensores - API con Flask + Docker

Este proyecto implementa una **API en Flask** que utiliza dos modelos de redes neuronales entrenados con TensorFlow/Keras para:

- 🔮 Predecir la temperatura que habrá en una hora.
- 🚪 Predecir si las ventanas o la puerta estarán abiertas.

---

## 🧠 Modelos utilizados

- `model_predict_temperaturas.h5`: modelo de regresión para temperatura futura.
- `model_predicciones_se_abrira.h5`: modelo de clasificación binaria (ventana/puerta abierta o no).

Ambos modelos están entrenados con variables meteorológicas y de sensores físicos.

---

## 📁 Estructura del proyecto


---

## 🚀 Cómo ejecutar localmente (sin Docker)

### 1. Crear entorno virtual y activarlo

```bash
python3 -m venv .venv
source .venv/bin/activate


docker pull younessdrfaustibarbera/sensores-api:latest
docker run -p 5000:5000 younessdrfaustibarbera/sensores-api:latest

