# 🏆 API de Predicción de Apertura de Ventanas

Esta API predice si **las ventanas estarán abiertas en la próxima hora** usando datos de sensores y condiciones meteorológicas. Para ello, realiza dos pasos:

1. **Predicción de temperatura futura interna** con un modelo de regresión.
2. **Predicción de apertura de ventanas** con un modelo de clasificación binaria, usando la temperatura estimada y otras variables.

---

## 📦 Estructura de la API

- Framework: `Flask`
- Modelos usados: 
  - `model_predict_temperaturas.keras` (regresión)
  - `model_predicciones_se_abrira.keras` (clasificación)

- Fuente de datos:  
  CSV alojado en GitHub:  
  [`entrenamiento_neuronal_calefaccion_gold.csv`](https://github.com/JHYouness/Mislata_proyecto/blob/main/data/data_gold/entrenamiento_neuronal_calefaccion_gold.csv)

---

## 🔍 Endpoint disponible

### `GET /predict_windows`

Realiza la predicción a partir del último registro.

#### Respuesta esperada:
```json
{
  "Predicción": [
    {
      "alerta": "En la próxima hora las ventanas estarán abiertas"
    }
  ]
}

#### Respuesta esperada en caso de que la calefacción este apagada:
```json
{
  "Predicción": [
    {
      "alerta": "En la próxima hora la calefacción estará apagada"
    }
  ]
}
```

> ⚠️ La predicción es booleana: `True` si se espera que las ventanas se abran, `False` en caso contrario.

---

## ⚙️ Lógica de preprocesamiento

- Se escalan las variables con `MinMaxScaler`.
- Se predice la temperatura con `modelo_temperaturas`.
- Se descartan registros donde la calefacción no esté activa.
- Se filtra solo de lunes a viernes y entre las 7:00 y las 21:00.
- El modelo de clasificación recibe 22 features (meteorológicas, solares, estacionales, etc.) + la temperatura predicha.
  
