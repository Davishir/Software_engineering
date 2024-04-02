# Тема 8. Введение в ООП.
Отчет по Теме #8 выполнил(а):
- Ширыкалова Дарья Витальевна
- ИНО ЗБ ПОАС-22-1

| Задание |  Сам_раб |
| ------ |  ------ |
| Задание 1 | + |
| Задание 2 | + |
| Задание 3 | + | 
| Задание 4 | + | 
| Задание 5 | + |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Самостоятельная работа №1
### Самостоятельно создайте класс и его объект.

```python
class Case: 
    def __init__(self,color):
        self.color=color
pensil = Case("blue") 

```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_8/png_8/1.png).


## Выводы
Класс пенал. Объект ручка.

## Самостоятельная работа №2
### Самостоятельно создайте атрибуты и методы для ранее созданного класса.

```python
class Case:
    def __init__(self,category,color):
        self.category=category
        self.color=color
pensil = Case("Ручка","black")
print(pensil.category)
print(pensil.color)
```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_8/png_8/2.png).

## Выводы

Атрибуты: категория,цвет.
  
## Самостоятельная работа №3
### Самостоятельно реализуйте наследование, продолжая работать ранее созданным классом. 

```python

class Case:
    def __init__(self,color):
        self.color=color

class Pen(Case): 
    def eat(self):
        print(f"{self.color} eats")

pencil = Case("Green")
print(pencil.color)


```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_8/png_8/3.png).

## Выводы

наследование класса Case
  
## Самостоятельная работа №4
### Самостоятельно реализуйте инкапсуляцию

```python
class Case:
    def __init__(self, category, color):
        self._category = category 
        self._color = color  


    def eat(self):
        print(f" В пеняле лежит {self._category} она {self._color} цвета")

pencil = Case("Ручка", "Синяя")
print(pencil._category)
pencil.eat()

```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_8/png_8/4.png).

## Выводы

В пенале лежит ручка она синего цвета.
  
## Самостоятельная работа №5
### Самостоятельно реализуйте полиморфизм. 


```python
class Case:
    def area(self):
        pass
class Pen(Case): 
    def __init__(self, category, color):
        self.category = category 
        self.color = color  
pencil = Pen("Ручка", "Синяя")

print("Pen category:", pencil.category)
print("Pen color:", pencil.color)

class Marker(Case): 
    def __init__(self, color):
        self.color = color  

mark = Marker("Pink")
print("Marker color:", mark.color)

```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_8/png_8/5.png).

## Выводы
Наследование класса Case
  


## Общие выводы по теме
ООП предоставляет набор концепций и методологий, позволяющих описывать, моделировать и взаимодействовать с объектами в программе.
