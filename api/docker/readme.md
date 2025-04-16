# 🌡️ API con Flask + Docker

Este proyecto implementa una **API en Flask** que utiliza dos modelos de redes neuronales entrenados con TensorFlow/Keras para:

- 🔮 Predecir la temperatura en la sala que determina la calefacción.
  
- 🚪 Predecir si las ventanas o la puerta estarán abiertas. (En caso de que la calefacción esté encendida)

---

## 🧠 Modelos utilizados

- `model_predict_temperaturas.keras`: modelo de regresión para temperatura futura.
- `model_predicciones_se_abrira.keras`: modelo de clasificación binaria (ventana/puerta abierta o no).

Ambos modelos están entrenados con variables meteorológicas y de sensores físicos.

---

## 🚀 Cómo ejecutar localmente 

### 1. Crear entorno virtual y activarlo

```bash
docker pull younessdrfaustibarbera/sensores-api:latest
docker run -p 5000:5000 younessdrfaustibarbera/sensores-api:latest

