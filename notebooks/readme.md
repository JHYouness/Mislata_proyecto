# 📓 Notebooks

Este directorio contiene los notebooks utilizados para el desarrollo, limpieza, análisis y entrenamiento de modelos.

## Contenido

### 🔹 `limpieza_silver.ipynb`
Limpieza de los datos provenientes de la capa *bronze*, generando la capa *silver*.

- Limpiamos y formateamos datos
- Agrupamos en 1 hora
- Eliminamos registros no disponibles
- Añadimos la y_true

---

### 🔹 `limpieza_gold.ipynb`
Notebook dedicado a la limpieza final de los datos antes de su uso en informes, dashboards o análisis exploratorios. Trabaja sobre los datos de la capa *gold*.

- Validación de formatos
- Eliminación de outliers restantes
- Normalización final de columnas
- Generación de dataset listo para visualización

---

### 🔹 `limpieza_modelo_temperatura.ipynb`
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
