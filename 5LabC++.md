**Київський Національний  університет імені Тараса Шевченка**

**Кафедра програмних систем і технологій**

**Звіт про виконання 5 лабораторної роботи  з дисципліни
“Основи програмування”**

**Виконав:** *Косенко Денис Русланович*

*студент 1 курсу ФІТ ІПЗ 13 групи*

**Викладач:**  *Поляков С.А. , Ковалюк Т.В.*

**Київ-2019**

## 7 варіант


- Задані натуральні числа а, c, m. Визначити рекурсивну функцію та глибину рекурсії для обчислення   за формулою:
де   - залишок від ділення   на 10.
 
 ```
#include "pch.h"
#include <iostream>
using namespace std;
#include <string>
void sort(string st)
{
	for (int i = 0; i < st.length(); i++)
		for (int j = 0; j < st.length(); j++)
		{
			int a = int(st[j]);
			int b = int(st[j + 1]);
			if (a > b)
			{
				char buf = st[j];
				st[j] = st[j + 1];
				st[j + 1] = buf;
			}
		}
	cout << st << "\n";
};
void main()
{
	string str = "asdfewrfwefd";
	sort(str);
}
