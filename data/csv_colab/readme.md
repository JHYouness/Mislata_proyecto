# 📁 Carpeta `csv_colab`

Esta carpeta contiene los ficheros CSV procesados durante las fases de limpieza de datos realizadas en Google Colab. Los archivos aquí presentes corresponden a una versión intermedia entre la extracción inicial y la transformación final.

## 📊 Flujo de trabajo de los datos

1. **Extracción**  
   Los datos originales se extraen desde la base de datos y se almacenan en la carpeta `data_bronze`. Esta etapa contiene los datos en su estado más crudo.

2. **Primera limpieza**  
   Desde `data_bronze`, se realiza una limpieza preliminar (desglosar los datos de la columna attribute). Los resultados de esta limpieza se almacenan en esta carpeta (`csv_colab`) para pruebas, validaciones y transformaciones adicionales.

## 🧹 Archivos en esta carpeta

- `*_limpio.csv`: Datos con limpieza básica aplicada.
- `*_agrupado.csv`: Datos agrupados por ciertas variables clave.
- `*_ok.csv`: Datos listos para ser trasladados a `data_silver`.

Cada archivo representa una entidad distinta (sensores, predicciones meteorológicas, etc.), y ha sido tratado individualmente según sus características.

## 📌 Nota
Este paso intermedio permite mantener la trazabilidad y facilita la detección de errores antes de mover los datos a entornos más controlados como `data_silver` o `data_gold`.

---

✍️ *Última actualización automática mediante Google Colab.*
