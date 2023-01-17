# Задание 1

### Код графика

```py
import numpy as np
import matplotlib.pyplot as plt

def f(x):
    return np.sin(x) * np.log2(x)

def find_ex():
    # Значение оси x,
    x = np.linspace(2 * np.pi, 3 * np.pi, 100)
    max_y = f(x[0])
    max_x = x[0]
    for i in range(1, len(x)):
            if f(x[i]) > max_y:
                max_y = f(x[i])
                max_x = x[i]
    return max_x

x = np.linspace(0*np.pi , 3*np.pi , 100 )
ex_x = find_ex()

# Рисуем в текущем рисованном объекте (ось x, ось y, имя нарисованной кривой, цвет линии, ширина линии)
plt.plot(x, f(x) , label="$f(x)$", color="b", linewidth=2)
plt.plot(ex_x, f(ex_x) ,  marker="x", color="r", linewidth=4)  #маркировка экстремума
plt.tick_params(labelcolor='r', labelsize='medium', width=3)

# X и Y координатное представление оси
plt.xlabel("Длинна")
plt.ylabel("Высота")

# Название диаграммы
plt.title("функция: y = sin(x) * log(x;2) и ее Экстремум")

# Показать изображение
plt.show()
```

### Сам график

![image](https://github.com/kriper2OO3/Lab-5/blob/main/Figure_1.png)
