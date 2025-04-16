# 📦 Codigo Models

Este directorio contiene los archivos relacionados con el entrenamiento y evaluación de modelos. Aquí es donde se lleva a cabo la fase de *modelado* tras la limpieza de los datos.

---

## 📘 Notebooks

### 🔹 `modelo_final.ipynb`

Notebook principal que entrena y guarda el modelo que predice si la puerta va a ser abierta en la siguiente hora.  
- Usa los datos procesados de la capa *gold* y los limpia ligeramente para que se adapten al problema.  
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
```bash
## Pruebas 
Final gold con toda la media:
R²: 0.8970504523554415
MAE: 0.648836102358483
MSE: 0.6529838609521241
RMSE: 0.8080741679772495

Con momento del dia sin hora
R²: 0.8970368943736906
MAE: 0.6489107417737588
MSE: 0.6530698559222134
RMSE: 0.8081273760504674

Con momento del dia con hora
R²: 0.8987227213493795
MAE: 0.6440411759081314
MSE: 0.6423770667583091
RMSE: 0.8014842897763556

Con momento del dia con hora + estación + mes
R²: 0.8991891485597262
MAE: 0.6412342730190507
MSE: 0.6394186327716259
RMSE: 0.7996365629282005

TODOS LOS SENSORES INDIVIDUALMENTE con momento del dia con hora + estación + mes
R²: 0.9109526008455173
MAE: 0.5952380537049661
MSE: 0.5648059252129447
RMSE: 0.7515357112026977

Con el sensor 2 Con momento del dia con hora + estación + mes
R²: 0.8729941155152129
MAE: 0.7152712484882678
MSE: 0.8055673357676888
RMSE: 0.8975340304231861

Con el sensor 3 Con momento del dia con hora + estación + mes
R²: 0.902240084872626
MAE: 0.6297751170016034
MSE: 0.6200672881693686
RMSE: 0.7874435142722103

Con el sensor 1 Con momento del dia con hora + estación + mes
R²: 0.9052256928588602
MAE: 0.6165286997809922
MSE: 0.6011303052029964
RMSE: 0.7753259348190259

Con el sensor 1 Con momento del dia con hora + estación + mes, sin filtrar diurno
R²: 0.9161500202526756
MAE: 0.5478644818516705
MSE: 0.4720345040813112
RMSE: 0.6870476723498241

Con el sensor 1 Con sol + momento del dia con hora + estación + mes, sin filtrar diurno
R²: 0.9168971491159181
MAE: 0.5459458600175886
MSE: 0.4678285328514038
RMSE: 0.6839799213803017
```

---

## Notas

- Los modelos están pensados para integrarse directamente con los pipelines definidos en `airflow/`.  
--- 

