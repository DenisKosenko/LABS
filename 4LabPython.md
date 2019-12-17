**Київський Національний  університет імені Тараса Шевченка**

**Кафедра програмних систем і технологій**

**Звіт про виконання 4 лабораторної роботи  з дисципліни
“Основи програмування”**

**Виконав:** *Косенко Денис Русланович*

*студент 1 курсу ФІТ ІПЗ 13 групи*

**Викладач:**  *Поляков С.А. , Ковалюк Т.В.*

**Київ-2019**

## 7 варіант

- Обчислити значення функції у, розвинувши функцію sh(x) у ряд Тейлора. Аргумент х змінюється від 0 до 3 з кроком 0.5. Визначити похибку 

````
import math
import pytest

num = -1
list = []

def func(x, n):

    number2 = 2 * n + 1   
    fact = math.factorial(number2)
    
    number1 = x **(2 * n + 1)
    step = number1 / fact

    list.append(step)

    global numsum
    numsum = sum(list)

    return numsum
    list.clear()

for i in range(0,4):
    num += 1
    func(i, num)

num = 0
one = numsum

for i in range(0,4):
    num += 1
    func(i ** 2, num)

num = 0
two = numsum
tree = one ** 2
num = 0

for i in range(0,4):

    num += 1   
    func(i + 2, num)

four = numsum

print("------------------------")
print(one)
print(two)
print(tree)
print(four)
print("------------------------")

result = (one + two) / (tree / four)

print(result)
