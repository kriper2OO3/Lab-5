# Задание 3

## Код золотого сечения
```py
import numpy as np

def f(x):
    return np.sin(x) * np.log2(x)


def golden_ratio(x1, x2, count=1):
    left = x2 - (x2 - x1) / 1.618
    right = x1 + (x2 - x1) / 1.618
    if abs(f(left) - f(right)) < 0.0001:
        print("Количество шагов:", count)
        return (left+right)/2
    if f(left) <= f(right):
        count = count + 1
        res = golden_ratio(left, x2, count)
    elif f(left) > f(right):
        count = count + 1
        res = golden_ratio(x1, right, count)
    return res


x1 = 2.*np.pi
x2 = 3.*np.pi
res_golden_ratio = golden_ratio(x1, x2)
res_f = f(res_golden_ratio)
print("X: {0:.4f}, Y: {1:.4f}".format(res_golden_ratio, res_f))
```

## Результаты работы программы

Количество шагов: 11
X: 7.9129, Y: 2.9790
