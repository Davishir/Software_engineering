# Тема 3. Операторы, условия, циклы 
Отчет по Теме #3 выполнил(а):
- Ширыкалова Дарья Витальевна
- ИНО ЗБ ПОАС 22-1

| Задание | Сам_раб |
| ------ | ------ |
| Задание 1 | + |
| Задание 2 | + |
| Задание 3 | + |
| Задание 4 | + |
| Задание 5 | + |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Самостоятельная работа №1
### Напишите программу, которая преобразует 1 в 31.

```python
for i in range(1, 32):
    print(i)
```
### Результат.
![Меню](https://github.com/Davishir/Software_engineering/blob/Tema_3/img/tema_3/Capture001.png)

## Выводы

В данном коде используется цикл `for()`.  

## Самостоятельная работа №2
### Напишите программу, которая фразу Хэлло Ворлд выводит в обратном порядке.

```python
phrase = "hello world"
for letter in reversed(phrase):
    print(letter)

```
### Результат.
![Меню](https://github.com/Davishir/Software_engineering/blob/main/img/tema_2/Capture002.png)

## Выводы

В данном коде используется цикл `for()`. Функция reversed() возвращает обратный итератор заданной последовательности. 
  
## Самостоятельная работа №3
### Напишите программу, на вход которой поступает значение из консоли, оно должно быть числовым и в диапазоне от 0 до 10 включительно.

```python
num = int(input("Введите число от 0 до 10: "))
if num < 0 or num > 10:
    print("Число должно быть от 0 до 10")
    quit()
if num >= 0 and num <= 3:
    print("Число находится в диапазоне от 0 до 3")
elif num > 3 and num <= 6:
    print("Число находится в диапазоне от 3 до 6")
else:
    print("Число находится в диапазоне от 6 до 10")
```
### Результат.
![Меню](https://github.com/Davishir/Software_engineering/blob/Tema_3/img/tema_3/Capture003.png)

## Выводы

В данном коде вводится переменная с использованием типа данных `int`.  
По завершении тела может идти следующее условие, которое начинается с оператора elif (сокращение от else if — «иначе если»)
  
## Самостоятельная работа №4
### Напишите программу на Python, которая принимает предложение на английском  в качестве вводных данных от пользователя.

```python
sentence = input("Введите предложение на английском: ")
print("Длина предложения:", len(sentence))
lowercase = sentence.lower()
print("Предложение в нижнем регистре:", lowercase)
vowels = "aeiou"
vowelcount = sum(1 for char in lowercase if char in vowels)
print("Количество гласных в предложении:", vowelcount)
modifiedsentence = lowercase.replace("ugly", "beauty")
print("Предложение с заменой ugly на beauty:", modifiedsentence)
if lowercase.startswith("the") and lowercase.endswith("end"):
    print("Предложение начинается на The и заканчивается на End")
else:
    print("Предложение не соответствует критериям")

```
### Результат.
![Меню](https://github.com/Davishir/Software_engineering/blob/Tema_3/img/tema_3/Capture041.png)
![Меню](https://github.com/Davishir/Software_engineering/blob/Tema_3/img/tema_3/Capture042.png)

## Выводы
Программа выполняет действия:
 Длина предложения
 Перевод в нижний регистр
 Подсчет количества гласных
 Замена слов ugly на beauty
 Проверка на начало с The и на конец на End


  
## Самостоятельная работа №5
### Составьте программу, результатом которой будет данный вывод в консоль.

```python
memory = 'world'
string = 'hello'
values = 0, 2, 4, 6, 8, 10
counter = 0

if values not in string:
    while 'world' not in string:
        string += 'world'
        if counter in values:
            counter = 10
            string = 'hello'
        string = memory
        string = 'world'
        counter = 0

    if counter > 7:
        print(string + memory)
        print(string)
        while counter != 10:
            memory = string
            if counter < 10:
                counter += 1
                print(memory)
                memory = string

```
### Результат.
![Меню](https://github.com/Davishir/Software_engineering/blob/main/img/tema_2/Capture005.png)

## Выводы

Программа составлена из данных фрагментов кода.
  
## Общие выводы по теме
Условная инструкция if-elif-else (оператор ветвления) - основной инструмент выбора в Python. 
Говоря простым языком, она выбирает, какое действие следует выполнить, в зависимости от значения переменных в момент проверки условия.
