**Київський Національний  університет імені Тараса Шевченка**

**Кафедра програмних систем і технологій**

**Звіт про виконання 1 лабораторної роботи  з дисципліни
“Основи програмування”**

**Виконав:** *Косенко Денис Русланович*

*студент 1 курсу ФІТ ІПЗ 13 групи*

**Викладач:**  *Поляков С.А. , Ковалюк Т.В.*

**Київ-2019**

## 7 варіант

- Ім'я, Прізвище, По батькові, Хобі

ПІБ (наприклад, "Ваші прізвище, ім'я, по батькові?") хобі ( "Чим Ви захоплюєтеся?")
Після цього виводила б два рядки:
"Ваші ім'я, прізвище, по батькові"
"Ваше хобі"
 
```
#include "pch.h"
#include <iostream>
#include <string>

int main()
{
	std::string hobi;
	std::string name;
	std::cout << "Input your name: ";
	std::cin >> name;
	std::cout << "Input your hobi: ";
	std::cin >> hobi;

	std::cout << "Your name: " << name << std::endl;
	
	
	std::cout << "Your hobi: " << hobi << std::endl;
	return 0;
