# 📓 Notebooks

Este directorio contiene el notebook principal de limpieza, coge los datos _raw_ y los formatea y limpia hasta dejarlos en .


# Notebook `Colab_sensores.ipynb`

## Contenido de Colab_sensores.ipynb
### 🔹 `Limpieza bronze`

- Formateamos los datos, dada la columna de atributos se desglosa y pivotamos con su contenido.

---

### 🔹 `Limpieza silver`
Limpieza de los datos provenientes de la capa *bronze*, generando la capa *silver*.

- Limpiamos y formateamos datos
- Agrupamos en 1 hora
- Eliminamos registros no disponibles
- Añadimos la y_true al dataframe principal

---

### 🔹 `Limpieza gold`
Notebook dedicado a la limpieza final de los datos antes de usarlo en entrenamiento de modelos. Trabaja sobre los datos de la capa *gold*.

- Sustituimos la entidad de forecast/mislata por la API de https://open-meteo.com/
- Limpiamos datos y nulos
- Creamos un modelo de regresión lineal para 

---


# Notebook `limpieza_modelo_temperatura.ipynb`
Preprocesamiento específico de los datos requeridos para entrenar un modelo de predicción de temperatura.

- Selección de variables relevantes
- Imputación de valores faltantes
- Ajustes específicos para modelado

---

### 🔹 `modelo_final.ipynb`
Notebook dedicado al entrenamiento, validación y evaluación del modelo predictivo principal (por ejemplo, predicción de temperatura).

- División train/test
- Entrenamiento del modelo
- Evaluación mediante métricas (RMSE, MAE, etc.)
- Exportación del modelo entrenado

---

## Requisitos

Asegúrate de haber instalado las dependencias listadas en el archivo raíz `requirements.txt` antes de ejecutar los notebooks.

---

## Notas

- Todos los notebooks están pensados para ser ejecutados en orden lógico: desde la limpieza inicial hasta la generación del modelo final.
- Se recomienda usar un entorno virtual y JupyterLab o VSCode para facilitar la ejecución.
