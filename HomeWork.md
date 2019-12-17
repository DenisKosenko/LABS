**Київський Національний  університет імені Тараса Шевченка**

**Кафедра програмних систем і технологій**

**Звіт про виконання домашньої роботи  з дисципліни
“Основи програмування”**

**Виконав:** *Косенко Денис Русланович*

*студент 1 курсу ФІТ ІПЗ 13 групи*

**Викладач:**  *Поляков С.А. , Ковалюк Т.В.*

**Київ-2019**
```
import turtle
import random

def s(l: list)->list:
     return l
     
print("Enter kolichestvo random kamnei")
kolichestvo = int(input())
list= []

chervone = 0
jovte = 0
sune = 0
zelene = 0

turtle.speed(5)

turtle.up()
turtle.goto(-350,0)
turtle.down()

turtle.pensize(5)

kolichestvo = int(input())
for i in range (0, kolichestvo):
    x = random.randint(1,4)

    if x == 1:
        list.append("ч")

        turtle.color("red")

        for storonu in range (0,4):
            turtle.forward(10)
            turtle.right(90)

        turtle.up()
        turtle.forward(20)
        turtle.down()

    elif x == 2:
        list.append("ж")

        turtle.color("yellow")

        for storonu in range (0,4):
            turtle.forward(10)
            turtle.right(90)

        turtle.up()
        turtle.forward(20)
        turtle.down()

    elif x == 3:
        list.append("с")

        turtle.color("blue")

        for storonu in range (0,4):
            turtle.forward(10)
            turtle.right(90)

        turtle.up()
        turtle.forward(20)
        turtle.down()

    elif x == 4:
        list.append("з")

        turtle.color("green")

        for storonu in range (0,4):
            turtle.forward(10)
            turtle.right(90)

        turtle.up()
        turtle.forward(20)
        turtle.down()

print(list)

list.sort()

print(list)

turtle.up()
turtle.goto(-350,0)
turtle.down()

poryadok = -1

for i in range (0, kolichestvo):
    poryadok += 1
    if list[poryadok] == "ж":
        turtle.color("yellow")

        for storonu in range(0, 4):
            turtle.forward(10)
            turtle.right(90)

        turtle.up()
        turtle.forward(20)
        turtle.down()

    elif list[poryadok] == "з":
        turtle.color("green")

        for storonu in range(0, 4):
            turtle.forward(10)
            turtle.right(90)

        turtle.up()
        turtle.forward(20)
        turtle.down()

    elif list[poryadok] == "с":
        turtle.color("blue")

        for storonu in range(0, 4):
            turtle.forward(10)
            turtle.right(90)

        turtle.up()
        turtle.forward(20)
        turtle.down()

    elif list[poryadok] == "ч":
        turtle.color("red")

        for storonu in range(0, 4):
            turtle.forward(10)
            turtle.right(90)

        turtle.up()
        turtle.forward(20)
        turtle.down()
```
**PyTest**
```
import random
import pytest

from dzKamni import s

chervone = 0
bile = 0
sune = 0
zelene = 0


@pytest.mark.parametrize(("inp", "out"), [
    ([chervone, sune, bile],[chervone, sune, bile])
])
def test_s(inp, out):
    assert s(inp) == out
