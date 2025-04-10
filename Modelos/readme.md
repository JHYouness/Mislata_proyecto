import matplotlib.pyplot as plt
import pandas as pd
df = pd.read_csv('/content/final_silver_v2.csv')

# Plot
plt.figure(figsize=(14, 6))
plt.plot(df['sensor.sensor_temperatura_1_temperature'], label='Sensor 1')
plt.plot(df['sensor.sensor_temperatura_2_temperature'], label='Sensor 2')
plt.plot(df['sensor.sensor_temperatura_3_temperature'], label='Sensor 3')
plt.plot(df['sensor.sensor_temperatura_4_temperature'], label='Sensor 4')
plt.plot(df['temperature ℃'], label='Temperature (℃)', linestyle='-.')

plt.xlabel('Time')
plt.ylabel('Temperature (℃)')
plt.title('Temperaturas en horario de calefacción')
plt.legend()
plt.grid(True)
plt.tight_layout()
plt.show()
