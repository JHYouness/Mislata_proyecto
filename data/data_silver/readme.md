# 📁 data_silver 🥈

Esta carpeta corresponde a la primera etapa (bronze) dentro de la metodología de gestión de datos (bronze-silver-gold).

## 📌 Objetivo de la carpeta

Esta carpeta contiene los datasets refinados o parcialmente transformados del proyecto, los datos han sido limpiados, integrados y estandarizados desde su forma original (bronze), pero aún no están completamente listos para el análisis final (gold).

## Estructura de la carpeta

- `Agrupation/`: Contiene datasets intermedios con agregaciones específicas por sensores o variables temporales.
- `Agrupation_Final/`: Subcarpeta con datasets listos para pasar a la fase "gold" tras aplicar transformaciones adicionales o imputaciones finales.
- `csv_colab/`: Archivos CSV generados o procesados en Google Colab, usados como apoyo en la fase silver.
- `Historico_temperaturas.csv`: Dataset con el histórico de temperaturas ambientales en la aula
- `final_silver.csv`: Versión consolidada de los datos en la capa silver antes de predecir sensores o aplicar sustituciones.
- `final_silver_sustituido.csv`: Versión con datos faltantes o erróneos ya sustituidos por valores estimados o interpolados.
- `final_silver_sensores_predichos.csv`: Contiene predicciones generadas para sensores ausentes, como ventanas o puertas abiertas.
- `final_silver_v2.csv`: Última versión de consolidación con todos los datos integrados, corregidos y listos para pasar a la capa gold.

## Propósito

La capa silver es fundamental para garantizar que los datos que lleguen a la fase de análisis final (gold) estén correctamente depurados. Aquí se realizan tareas como:

- Corrección de valores erróneos
- Sustitución de datos faltantes
- Integración de fuentes heterogéneas
- Predicción de variables ausentes
- Generación de datasets consolidados y temporales
