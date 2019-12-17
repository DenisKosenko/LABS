**Київський Національний  університет імені Тараса Шевченка**

**Кафедра програмних систем і технологій**

**Звіт про виконання індтвідуальної роботи  з дисципліни
“Основи програмування”**

**Виконав:** *Косенко Денис Русланович*

*студент 1 курсу ФІТ ІПЗ 13 групи*

**Викладач:**  *Поляков С.А. , Ковалюк Т.В.*

**Київ-2019**

## 35 варіант
```
import random
a, b = [], []
print("Enter x matr")
print("----------------------")
matr = int(input())
for i in range(matr):
    for j in range(matr):
        x = random.randint(0,9)
        b.append(x)

    a.append(b)
    print(a[i])
    b = []
print("----------------------")


print("str1: ")
str1 = int(input())
print("str2: ")
str2 = int(input())

if str1 <= matr and str2 <= matr:
    one = a[str1-1]
    two = a[str2 -1]
    a[str1-1] = two
    a[str2-1] = one

    print("----------------------")
    for i in range(0,matr):
        print(a[i])


print("row1")
row1 = int(input())
print("row2")
row2 = int(input())

print("----------------------")

r1 = []
r2 = []
for h in range(0,matr):
    r1.append(a[h][row1-1])

    r2.append(a[h][row2 - 1])
    a[h][row2-1] = r1[h]
    a[h][row1 - 1] = r2[h]
    print(a[h])

print("----------------------")

matr3 = 3
a1, b1, c1 = [], [], []
kmat = int(input("Kolichestvo matr:"))
for t in range(0,kmat):
    for i in range(matr3):
        for j in range(matr3):
            x1 = random.randint(0,9)
            b1.append(x1)
        a1.append(b1)
        b1 = []
    c1.append(a1)
    a1 = []

d = []
for i in range(0, kmat):
    j = i + 1
    r = i + 1
    if r <= kmat and j <= kmat:

        c1[r][0][0] = c1[i][0][0] * c1[j][0][0] + c1[i][0][1] * c1[j][1][0] + c1[i][0][2] * c1[j][2][0]   #c11 = a11 · b11 + a12 · b21 + a13 · b31 =
        c1[r][0][1] = c1[i][0][0] * c1[j][0][1] + c1[i][0][1] * c1[j][1][1] + c1[i][0][2] * c1[j][2][1]   #c12 = a11 · b12 + a12 · b22 + a13 · b32 =
        c1[r][0][2] = c1[i][0][2] * c1[j][0][0] + c1[i][0][1] * c1[j][1][2] + c1[i][0][2] * c1[j][2][2]   #c13 = a11 · b13 + a12 · b23 + a13 · b33 =
        c1[r][1][0] = c1[i][1][0] * c1[j][0][0] + c1[i][1][1] * c1[j][1][0] + c1[i][1][2] * c1[j][2][0]   #c21 = a21 · b11 + a22 · b21 + a23 · b31 =
        c1[r][1][1] = c1[i][1][0] * c1[j][0][1] + c1[i][1][1] * c1[j][1][1] + c1[i][1][2] * c1[j][2][1]   #c22 = a21 · b12 + a22 · b22 + a23 · b32 =
        c1[r][1][2] = c1[i][1][0] * c1[j][0][2] + c1[i][1][1] * c1[j][1][2] + c1[i][1][2] * c1[j][2][2]   #c23 = a21 · b13 + a22 · b23 + a23 · b33 =
        c1[r][2][0] = c1[i][2][0] * c1[j][0][0] + c1[i][2][1] * c1[j][1][0] + c1[i][1][0] * c1[j][2][0]   #c31 = a31 · b11 + a32 · b21 + a33 · b31 =
        c1[r][2][1] = c1[i][2][0] * c1[j][0][1] + c1[i][2][1] * c1[j][1][1] + c1[i][2][2] * c1[j][2][1]   #c32 = a31 · b12 + a32 · b22 + a33 · b32 =
        c1[r][2][2] = c1[i][2][2] * c1[j][0][2] + c1[i][2][1] * c1[j][1][2] + c1[i][2][2] * c1[j][2][2]   #c33 = a31 · b13 + a32 · b23 + a33 · b33 =
    else:
        break
    for e in range(0, kmat):
        for y in range(0, matr3):
            print(c1[e][y])
        print("----------------------")
    print("----------------------")
