import pandas as pd
import numpy as np
data = {
    'Average_Pulse': [80, 90, 100, 110, 120],
    'Calorie_Burnage': [150, 200, 250, 300, 350]
}
health_data = pd.DataFrame(data)
x = health_data["Average_Pulse"]
y = health_data["Calorie_Burnage"]
slope_intercept = np.polyfit(x, y, 1)
print(slope_intercept)


def slope(x1, y1, x2, y2):
    s = (y2 - y1) / (x2 - x1)
    return s
print(slope(2, 5, 6, 15))


import matplotlib.pyplot as plt
import numpy as np
x = np.array([1, 2, 3, 4, 5])  # Первая переменная (например, время)
y = np.array([2, 3, 5, 4, 6])  # Вторая переменная (например, количество продаж)
m, b = np.polyfit(x, y, 1)  # Получение параметров наклона и сдвига
plt.scatter(x, y, color='blue', label='Данные')  # График данных
plt.plot(x, m * x + b, color='red', label='Линейная функция')  # Линейная функция
plt.title('Линейная зависимость между переменными')
plt.xlabel('Первая переменная')
plt.ylabel('Вторая переменная')
plt.legend()
plt.grid(True)
plt.show()

