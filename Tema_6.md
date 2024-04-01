# Тема 6. Базовые коллекции: словари, кортежи.
Отчет по Теме #6 выполнил(а):
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
### При создании сайта у вас возникла потребность обрабатывать данные пользователя в странной форме, а потом переводить их в нужные вам форматы.

```python
user_input = input("Введите последовательность чисел, разделенных пробелом: ")

numbers = user_input.split()

numbers_list = list(map(int, numbers))
numbers_tuple = tuple(map(int, numbers))

print("Список из введенных чисел:", numbers_list)
print("Кортеж из введенных чисел:", numbers_tuple)

```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_6/png_6/1.png).


## Выводы
данные от пользователя. Разбиваем введенную строку на отдельные числа.Преобразуем последовательность чисел в список и кортеж.
Выводим полученный список и кортеж.

## Самостоятельная работа №2
### Николай знает, что кортежи являются неизменяемыми, но он очень упрямый и всегда хочет доказать, что он прав. 

```python
def remove_first_element(tup, element):
    if element in tup:
        index = tup.index(element)
        new_tup = tup[:index] + tup[index+1:]
        return tuple(new_tup)
    return tup
inputs = [(1, 2, 3, 1), (1, 2, 3, 1, 2, 3, 4, 5, 2, 3, 4, 2, 4, 2), (2, 4, 6, 6, 4, 2)]
elements = [1, 3, 9]

for idx, tup in enumerate(inputs):
    element = elements[idx]
    result = remove_first_element(tup, element)
    print(f"Для входных данных {tup} и элемента {element}: {result}")

```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_6/png_6/2.png).

## Выводы
Примеры входных данных и ожидаемых результатов. Проход по каждому примеру.

  
## Самостоятельная работа №3
### Ребята поспорили кто из них одним нажатием на numpad наберет больше повторяющихся цифр, но не понимают, как узнать победителя. 

```python
from collections import Counter
def most_common_numbers(digits_str):
    digits_count = Counter(digits_str)

    most_common = digits_count.most_common(3)

    top3_most_common = {int(num): count for num, count in most_common}

    return dict(sorted(top3_most_common.items()))

digits_string = "137512746554512"

result_dict = most_common_numbers(digits_string)


for key in sorted(result_dict.keys()):
    print(f"Цифра: {key}, Количество: {result_dict[key]}")

```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_6/png_6/3.png).

## Выводы
Создаем словарь, содержащий количество каждой цифры в строке. Получаем три самые часто встречаемые цифры в порядке убывания их количества. Создаем словарь из топ-3 самых часто встречаемых чисел. Пример строки с числами. Получаем словарь из трех самых часто встречаемых чисел.
  
## Самостоятельная работа №4
### Ваш хороший друг владеет офисом со входом по электронным картам, ему нужно чтобы вы написали программу, которая показывала в каком порядке сотрудники входили и выходили из офиса. 

```python
def find_employee_records(records, employee_id):
    start_index = -1
    end_index = -1
    count = 0
    for i, record in enumerate(records):
        if record == employee_id:
            count += 1
            if count == 1:
                start_index = i
            if count == 2:
                end_index = i

    if start_index == -1:
        return ()
    if end_index == -1:
        return records[start_index:]

    return records[start_index:end_index + 1]

print(find_employee_records((1, 2, 3),8))  
print(find_employee_records((1, 8, 3, 4, 8, 8, 9, 2),8,))  
print(find_employee_records((1, 2, 8, 5, 1, 2, 9), 8))  


```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_6/png_6/4.png).

## Выводы
Примеры. Результат: (2, 3, 2). Результат: (3, 4, 5).  Результат: (6, 1, 2, 9).

  
## Самостоятельная работа №5
### Самостоятельно придумайте и решите задачу, в которой будут обязательно использоваться кортеж или список. 

```python
def tuple_sort(tpl):
    for elm in tpl:
        if not isinstance(elm, int):
            return tpl
    return tuple(sorted(tpl))

if __name__ == '__main__':
    print(tuple_sort((9, 7, 3, 1, 144)))
    print(tuple_sort((8, 5, 2.16, 6)))
    print(tuple_sort((2, 9, '1', 18)))

```
### Результат.
![Меню](https://github.com/Dar13lol/Software_Engineering/blob/Laba_6/png_6/5.png).

## Выводы

Функция, которая будет сортировать кортеж, состоящий из целых чисел по возрастанию, и возвращает его.
Если хотя бы один элемент не является целым числом, то функция возвращает исходный кортеж

## Общие выводы по теме
 Словари в Python обозначаются фигурными скобками { и используются для хранения и доступа к данным с помощью ключей. Кортежи как параметры функций и их использование в качестве возвращаемых значений являются полезным инструментом для передачи и получения нескольких значений одновременно. 
