# Тема 5: Структуры данных
Информацию об основных структурах данных и типах коллекций можно посмотреть [здесь](../2/README.md). \
Здесь же мы рассмотрим особенности работы с модулем `collections` в `Python`

## Введение в модуль `collections`

Модуль `collections` является частью стандартной библиотеки Python и предоставляет дополнительные структуры данных, которые расширяют возможности базовых встроенных контейнеров, таких как списки и словари. Эти дополнительные структуры данных могут быть полезны в различных задачах программирования.

## Применение модуля `collections`

### `namedtuple`

`namedtuple` предоставляет именованные кортежи, которые объединяют преимущества кортежей и именованных полей. Это полезно для создания простых структур данных.

Пример использования `namedtuple`:

```python
from collections import namedtuple

Person = namedtuple('Person', ['name', 'age'])
person = Person(name='Alice', age=30)

print(person.name)  # Выведет 'Alice'
print(person.age)   # Выведет 30
```

### `defaultdict`

`defaultdict` - это словарь, в котором значениями по умолчанию являются объекты заданного типа. Это удобно, когда вы хотите избежать проверок наличия ключей в словаре.

Пример использования `defaultdict`:

```python
from collections import defaultdict

word_count = defaultdict(int)
text = "Python is a powerful programming language."

for word in text.split():
    word_count[word] += 1

print(word_count['Python'])  # Выведет 1
print(word_count['is'])      # Выведет 1
print(word_count['Java'])    # Выведет 0 (по умолчанию)
```

### `Counter`

`Counter` - это контейнер, предназначенный для подсчета элементов в итерируемых объектах. Это полезно для подсчета частоты встречаемости элементов.

Пример использования `Counter`:

```python
from collections import Counter

colors = ['red', 'blue', 'red', 'green', 'blue', 'red']

color_count = Counter(colors)
print(color_count)  # Выведет Counter({'red': 3, 'blue': 2, 'green': 1})
```

### `deque`

`deque` предоставляет двунаправленную очередь, что обеспечивает быстрое добавление и удаление элементов с обоих концов. Это полезно для реализации стеков и очередей.

Пример использования `deque`:

```python
from collections import deque

queue = deque()
queue.append(1)
queue.append(2)
queue.append(3)

print(queue.popleft())  # Выведет 1
print(queue.popleft())  # Выведет 2
```

## Лучшие практики при использовании модуля `collections`

1. **Используйте `namedtuple` для создания простых структур данных.** Это делает ваш код более читаемым и понятным.

2. **Используйте `defaultdict` для предотвращения ошибок при доступе к значениям словаря.** Это улучшает безопасность и уменьшает необходимость в проверках наличия ключей.

3. **Используйте `Counter` для подсчета элементов в итерируемых объектах.** Это облегчает анализ данных и поиск наиболее часто встречающихся элементов.

4. **Используйте `deque` для эффективной реализации структур данных, таких как стеки и очереди.** Это повышает производительность и улучшает читаемость кода.


## Литература
1. [collections — Container datatypes](https://docs.python.org/3/library/collections.html)