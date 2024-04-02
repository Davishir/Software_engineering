# Тема 9. Концепции и принципы ООП.
Отчет по Теме #9 выполнил(а):
- Ширыкалова Дарья Витальевна
- ИНО ЗБ ПОАС-22-1

| Задание |  Сам_раб |
| ------ |  ------ |
| Задание 1 | + |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Самостоятельная работа №1
### Задание Садовник и помидоры

```python
class Tomato:
    states = {
        0: "растет",
        1: "цветет",
        2: "зеленый",
        3: "красный"
    }

    def __init__(self, index):
        self._index = index  
        self._state = self.states[0]  

    def grow(self):
        if self._state != self.states[len(self.states) - 1]:  
            current_state_index = list(self.states.values()).index(self._state)
            self._state = self.states[current_state_index + 1]  

    def is_ripe(self):
        return self._state == self.states[len(self.states) - 1]  

class TomatoBush:
    def __init__(self, num):
        self.tomatoes = [Tomato(index) for index in range(1, num + 1)]  

    def grow_all(self):
        for tomato in self.tomatoes:
            tomato.grow()  

    def all_are_ripe(self):
        return all([tomato.is_ripe() for tomato in self.tomatoes])  

    def give_away_all(self):
        self.tomatoes = []  

class Gardener:
    def __init__(self, name, plant):
        self.name = name  
        self.plant = plant  

    def work(self):
        self.plant.grow_all()  

    def harvest(self):
        if self.plant.all_are_ripe():
            self.plant.give_away_all()  
        else:
            print("Еще не все помидоры созрели, продолжайте ухаживать за ними.")  

    @staticmethod
    def knowledge_base():
        print("База знаний по садоводству:\n...")  

# Тесты
# 1
Gardener.knowledge_base()  

# 2
bush = TomatoBush(5) 
gardener = Gardener("Вася", bush)  

# 3
gardener.work()  
# 4
gardener.harvest()  

# 5
gardener.work()  
gardener.work()
gardener.work()
gardener.harvest()  


```
### Результат.
![Меню](https://github.com/Davishir/Software_engineering/blob/Tema_9/img/tema_9/Capture001.png)


## Выводы

Инициализация индекса помидора. Инициализация состояния помидора. Проверка, не достиг ли помидор последнего состояния. Увеличение состояния помидора на один уровень. Проверка, созрел ли помидор.Создание списка помидоров. Увеличение состояния всех помидоров.Проверка, все ли помидоры созрели. Отдача собранных помидоров.Инициализация имени садовника. Инициализация объекта класса TomatoBush. Работа садовника (увеличение состояния всех помидоров). Сбор созревших помидоров. Вывод сообщения, если не все помидоры созрели. Вывод базы знаний о садоводстве. Вывод базы знаний. Создание коллекции помидоров. Создание садовника. Садовник работает. Садовник собирает созревшие помидоры. Садовник продолжает работу. Садовник собирает помидоры еще раз.

  


## Общие выводы по теме
Классы являются основным строительным блоком объектно-ориентированного программирования в Python. Они позволяют создавать объекты, которые являются экземплярами класса, и определять, как эти объекты будут работать и взаимодействовать. 
