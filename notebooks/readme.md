# 📓 Notebooks

Este directorio contiene el notebook principal de limpieza, coge los datos _raw_ y los formatea y limpia hasta dejarlos en .


# Notebook `Colab_sensores.ipynb`

### 🔹 `Limpieza bronze`

- Formateamos los datos, dada la columna de atributos se desglosa y pivotamos con su contenido.


### 🔹 `Limpieza silver`
Limpieza de los datos provenientes de la capa *bronze*, generando la capa *silver*.

- Limpiamos y formateamos datos
- Agrupamos en 1 hora
- Eliminamos registros no disponibles
- Añadimos la y_true al dataframe principal



### 🔹 `Limpieza gold`
Notebook dedicado a la limpieza final de los datos antes de usarlo en entrenamiento de modelos. Trabaja sobre los datos de la capa *gold*.

- Sustituimos la entidad de forecast/mislata por la API de https://open-meteo.com/
- Limpiamos datos y nulos
- Creamos un modelo de regresión lineal para generar los datos faltantes del sensor 3.

---

## Notas

- Todos los notebooks están pensados para ser ejecutados en orden lógico: desde la limpieza inicial hasta la generación del df final.
- El desarrollo de estos notebooks se ha hecho usando tanto VSCode en local como Colab, sincronizandose en Github con la ayuda de Airflow.
