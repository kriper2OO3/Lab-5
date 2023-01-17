# Задание 4


```py

def find_line(fw):
    for i in range(len(words)):
        if words[i] == fw:
            return i  # вернуть позицию слова
    return -1


def find_bin_rec(fw, x, y):  # recursia
    if x == y and words[x] != fw: return -1
    m = x + (y-x)//2
    if fw == words[m]: return m
    if fw > words[m]: return find_bin_rec(fw, m+1, y)
    if fw < words[m]: return find_bin_rec(fw, x, m-1)
    
    
def find_word(text, word):
    left = 0
    right = len(text) - 1
    while True:
        mid = (left + right) // 2
        if text[mid] == word:
            return "Слово на позиции: {0}".format(mid + 1)
        if (mid < left or mid > right):
            return "Нет слова в словаре"
        if text[mid] < word:
            left = mid + 1
        else:
            right = mid - 1


Количество шагов: 11
X: 7.9129, Y: 2.9790
