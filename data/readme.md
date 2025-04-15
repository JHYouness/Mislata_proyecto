# 📁 data/

Este directorio contiene todos los datasets utilizados a lo largo del proyecto, organizados en distintas capas de procesamiento: *bronze*, *silver* y *gold*.  
Cada carpeta representa una fase en el ciclo de vida de los datos, desde su forma cruda hasta su versión final lista para modelado.

---

## 🗂️ Estructura

```bash
data/
├── data_bronze/      # Datos crudos (raw)
├── data_silver/      # Datos limpiados y transformados
├── data_gold/        # Datos listos para entrenamiento y análisis
└── test/             # Archivos de prueba y validación
```

---

## 🧩 Capas de Datos

### 🔸 `data_bronze/`

- Contiene los CSV directamente obtenidos de sensores o fuentes externas.  
- Formato sin procesar, tal cual están en la base de datos de Timescale.  
- Incluye datos con errores, columnas no relevantes, formatos inconsistentes, etc.
  
---

### 🔸 `data_silver/`

- Datos formateados, estructurados y filtrados.  
- Se han eliminado nulos, outliers obvios, y se ha homogenizado el formato.  
- En esta capa se agregan y transforman columnas, y se aplican agrupaciones por hora.

---

### 🔸 `data_gold/`

- Datos finales listos para alimentar los modelos.  
- Ya se han imputado valores faltantes, normalizado atributos y cruzado información relevante (sensores + clima, por ejemplo).  

---

### 🔍 `test/`

- Datos usados para validación y pruebas durante el desarrollo.  
- Usado para probar pipelines y notebooks sin afectar datos principales.
