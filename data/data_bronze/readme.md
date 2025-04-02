# 📁 Data Bronze

Esta carpeta corresponde a la primera etapa (bronze) dentro de la metodología de gestión de datos (bronze-silver-gold).

## 📌 Objetivo de la carpeta

La carpeta \`data_bronze\` contiene los datos originales (o mínimamente transformados) obtenidos directamente desde las fuentes externas, sensores o sistemas operacionales. Los datos aquí almacenados tienen un formato básico (CSV), tal como fueron recogidos, con poca o ninguna limpieza aplicada.

## 📄 Contenido actual

### 1. **CSV_datos_Sol.csv**
Datos relacionados con información solar capturados desde la fuente original. Incluyen métricas como la irradiancia, temperatura ambiente, etc.

### 2. **entidad_sensor_mislata.csv**
Información recopilada desde sensores específicos localizados en Mislata. Incluye lecturas ambientales, calidad del aire, temperatura, humedad, entre otros.

### 3. **entidad_sensor_sensor.csv**
Dataset con lecturas generales obtenidas de diversos sensores. incluye mediciones de temperatura, presión, humedad y otros datos ambientales capturados en tiempo real.

### 4. **entidad_weather_forecast.csv**
Contiene datos de predicción meteorológica proporcionados por fuentes externas. Los datos pueden incluir previsiones de temperatura, lluvia, viento, etc.

## 🚩 Próximos pasos

Los datos de esta carpeta serán procesados y limpiados para pasar a la capa \`data_silver\`, donde se almacenarán versiones más estructuradas y limpias para su posterior análisis y visualización en \`data_gold\`.

---

📌 **Nota:** Mantén esta carpeta con los datos originales sin modificaciones significativas. Cualquier transformación o limpieza profunda deberá realizarse en etapas posteriores (silver o gold).
EOF
