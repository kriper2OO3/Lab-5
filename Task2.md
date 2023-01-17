# Задание 2

## Код тернарного поиска
```py
import numpy as np

def f(x):
    return np.sin(x) * np.log2(x)

def ternary_search(x1, x2, count = 1):
    left = x1 + (x2 - x1) / 3
    right = x2 - (x2 - x1) / 3
    if abs(f(left) - f(right)) < 0.0001:
        print("Количествово шагов:", count)
        return (left+right)/2
    if f(left) < f(right):
        count = count + 1
        res = ternary_search(left, x2, count)
    elif f(left) > f(right):
        count = count + 1
        res = ternary_search(x1, right, count)
    elif f(left) == f(right):
        count = count + 1
        res = ternary_search(left, right, count)
    return res

x1 = 2.*np.pi
x2 = 3.*np.pi
res_ternary_search = ternary_search(x1, x2)
res_f = f(res_ternary_search)
print("X: {0:.4f}, Y: {1:.4f}".format(res_ternary_search, res_f))
```

## Результаты работы программы

Количествово шагов: 12
X: 7.9170, Y: 2.9790
