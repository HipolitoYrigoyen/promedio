# 🌡️ Cálculo y Visualización del Promedio de Temperaturas de Lunes a Domingo

Este programa en Python calcula el promedio de la temperatura de lunes a domingo y lo visualiza utilizando **Seaborn**. A continuación, te mostramos el código:

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# 📅 Crear un DataFrame con datos ficticios de temperaturas
data = {
    'dia': ['Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sábado', 'Domingo'],
    'temperatura': [22, 24, 23, 25, 26, 27, 28]
}

df = pd.DataFrame(data)

# 🔍 Calcular el promedio de temperatura
promedio_temperatura = df['temperatura'].mean()
print(f"El promedio de temperatura de lunes a domingo es: {promedio_temperatura:.2f}°C")

# 📊 Visualizar el promedio usando seaborn
plt.figure(figsize=(8, 5))
sns.barplot(x='dia', y='temperatura', data=df, estimator='mean', ci=None)
plt.axhline(promedio_temperatura, color='red', linestyle='--', label='Promedio Temperatura')
plt.title('Promedio de Temperatura de Lunes a Domingo')
plt.xlabel('Día')
plt.ylabel('Temperatura (°C)')
plt.legend()
plt.show()
# 🔍 Programa en Python

![image](https://github.com/user-attachments/assets/0fe68ea5-1329-4a2d-baed-4a7775374c25)

# 🔍 Gráfico

![image](https://github.com/user-attachments/assets/842264e4-76ec-4b09-8f96-9df5c85ba3df)

