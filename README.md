# 🌱 Proyecto Eficiencia Energética

Este proyecto tiene como objetivo mejorar la eficiencia energética en nuestro centro educativo mediante la monitorización y análisis del uso de la calefacción y el aire acondicionado en las aulas. 
Se utilizan sensores IoT y técnicas de análisis de datos para detectar situaciones en las que se pierde energía, como puertas o ventanas abiertas mientras el sistema de climatización está encendido.

---

## 🏗️ Arquitectura del Sistema

### Componentes Principales

- **Home Assistant**: Servidor domótico que centraliza y visualiza todos los datos.
- **TimescaleDB**: Base de datos PostgreSQL optimizada para series temporales.
- **Mosquitto**: Broker MQTT open source.
- **Zigbee2MQTT**: Pasarela Zigbee ↔ MQTT.
- **SLZB-06**: Antena Zigbee a Ethernet.
- **Sensores**:
  - `Aqara MCCGQ11LM`: Sensor de puertas y ventanas.
  - `Aqara WSDCGQ11LM`: Sensor de temperatura, humedad y presión.
  - `Shelly Pro EM-50`: Sensor de corriente eléctrica.
- **Sistemas Climatización**:
  - Temperatura de la calefacción del centro.
  - Aire acondicionado del aula.
- **Integraciones en Home Assistant**:
  - `Meteorologisk institutt (Met.no)`: Datos meteorológicos externos.
  - `Sun`: Posición solar.

---

## 🖥️ Infraestructura

### 🔧 Servidor Principal

- **IP**: `172.16.204.240`

### 🏠 Home Assistant

- **URL**: [http://172.16.204.240:8123](http://172.16.204.240:8123)

### 📡 Mosquitto (MQTT Broker)

- **Puerto**: `1883`

### 🔁 Zigbee2MQTT

- **URL**: [http://172.16.204.240:8080](http://172.16.204.240:8080)

### 📶 SLZB-06

- **URL**: [http://172.16.204.241](http://172.16.204.241)

### 🗄️ TimescaleDB

- **Puerto**: `5432`
- **Base de Datos**: `postgres`

---

## 📋 TODO List del Proyecto

### ✅ Tarea 1: Objetivo del Proyecto

- ¿Qué se quiere predecir?
- ¿Cómo detectar pérdidas de energía?

---

### 📊 Tarea 2: Recopilación de Datos

- Agrupación por horas.
- Resumen de sensores por hora:
  - Temperatura, presión, humedad.
  - Estado de puertas y ventanas.
  - Temperatura de la calefacción.
  - Datos extra...

---

### 🌡️ Tarea 3: Temperatura del Aula

Definir cómo representamos la temperatura del aula:

- ¿Media de todos los sensores?
- ¿O cada sensor por separado?

---

### 🔗 Tarea 4: Correlaciones entre Sensores de Temperatura

- Analizar redundancia de sensores.
- Posibilidad de reducir el número de sensores necesarios.

---

### 🚪 Tarea 5: Correlaciones entre Sensores de Puertas/Ventanas

- Análisis similar al anterior.
- Optimización del número de sensores necesarios.

---

### 🔥 Tarea 6: Detección de Calefacción Encendida

Modelar si la calefacción está activa según los datos:

- Modelos:
  - ML lineal.
  - Red neuronal.
- Variables:
  - Temperatura (media o individual).
  - Nubosidad.
  - Posición del sol.
  - Temperatura exterior.
- Validación para evitar sobreajuste.

---

### 🧠 Tarea 7: Definición de Datos para IA

- Establecer:
  - Variables de entrada (features).
  - Variable objetivo (target).

---

### 🧪 Tarea 8: Creación del Modelo de IA

- Comparar:
  - Machine Learning clásico.
  - Redes neuronales.
- Evaluar precisión y sobreajuste.

---

## 📦 Extra

### 🌀 Apache Airflow

- **URL**: [http://localhost:8080](http://localhost:8080)
- **Descripción**: Utilizado para la orquestación y ejecución de procesos ETL mediante DAGs en entorno local.

### 📬 Postman

- **Uso**: Herramienta empleada para realizar peticiones HTTP a la API desarrollada y comprobar su correcto funcionamiento.

### 🐳 Docker

- **Uso**: Se ha utilizado para contenerizar el modelo de predicción. El contenedor ha sido subido a Docker Hub y se realizan peticiones al modelo desde Postman.

---

## 👩‍🏫 Participantes

Este proyecto se ha desarrollado por un grupo de estudiantes del curso de especializacion de Inteligencia Artificial y Big Data:
- Youness El Jylaly
- Yeray Rubio
- Gabriel Rodriguez
- Pablo Calvo
  
---

## 📁 Estructura del Repositorio
```bash
Mislata_proyecto-main/
├── airflow/                     # Definición de DAGs para ETLs
├── api/                         # Código de la API en flask
├── data/
│   ├── data_bronze/             # Datos crudos
│   ├── data_silver/             # Datos transformados e imputados
│   ├── data_gold/               # Datos listos para informes y dashboards
│   └── test/                    # Archivos de prueba
├── docs/                        # Documentación complementaria
├── models/                      # Modelos de IA entrenados
│   └── Codigo Models/           # Entrenamiento de los modelos y últimos retoques a los datos
├── notebooks/                   # Análisis y notebooks de desarrollo
├── token                        # Token de autenticación
├── README.md                    # Este archivo
└── requirements.txt             # Dependencias del proyecto
