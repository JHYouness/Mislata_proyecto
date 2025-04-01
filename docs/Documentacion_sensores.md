# Proyecto: Monitoreo de Sensores y Predicción de Temperatura

## Consultas útiles

### 1. Mostrar variables con valores nulos
```sql
SELECT * FROM ltss WHERE STATE LIKE 'unavailable';
``` 
### 2. Mostrar información sobre el estado del sol
```sql
SELECT * FROM ltss WHERE entity_id LIKE '%sun.sun%';
```
### Pasos a seguir
#### 1. Determinar si el radiador está encendido 
para ello, necesitamos:
- Obtener la temperatura exterior detectada por el termometro
- Esta informacion se proporciona proximamente
- Una vez la tengamos, podremos desarrollar un modelo para predecir la temperatura esperada y detectar si el radiador esta afectando el ambiente interior
#### 2. Avisar si las ventanas o puertas están abiertas
- Si una ventana o puerta permanece abierta durante 10 minutos acumulados, se debe notificar al jefe de estudios.
- No es necesario que los 10 minutos sean continuos; se debe acumular el tiempo total de apertura.
- Se evaluará si es mejor notificar a los 5 minutos en lugar de 10.
#### 3. Prescindir de sensores innecesarios 
- El objetivo es minimizar el número de sensores utilizados, manteniendo la funcionalidad del sistema.

## Variables interesantes
- `sensor.mislata`
- `sensor.sensor`
- `sun.sun`
- `weather.forecast`

## Unidades de medida deseadas

| Unidad | Descripción |
|--------|-------------|
| `°C`   | Grados Celsius. Se utiliza para medir la temperatura. |
| `hPa`  | Hectopascales. Unidad de presión atmosférica. 1 hPa = 100 pascales. Común en meteorología. |
| `%`    | Porcentaje. Usado para medir la humedad relativa del aire. |
