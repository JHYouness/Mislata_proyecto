# 🌀 Proyecto Airflow - Limpieza ETL para Mislata

Este módulo forma parte del proyecto `Mislata_proyecto`, y está dedicado a la ejecución de tareas ETL automatizadas utilizando Apache Airflow.

---

## 🚀 Descripción del flujo ETL

1. **Descarga de archivos CSV desde GitHub**
2. **Transformación de datos (limpieza, desanidamiento de columnas JSON, etc.)**
3. **Subida de archivos limpios nuevamente al repositorio en la carpeta `data/test`**

---

## ⚙️ Requisitos

Asegúrate de tener un entorno virtual con las siguientes dependencias:

```bash
pip install -r notebooks/requirements.txt
```

## 📁 Estructura de carpetas

``` bash
airflow/
├── dags/
├── notebooks/
├── logs/
├── docs/
└── airflow.cfg
```

