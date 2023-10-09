# Тема 2: Типы данных и операторы в Python

## Основные типы данных
1. **Числа:**
   - Целые числа (int): Целые числа без десятичной точки, например, 5, -10.
   - Числа с плавающей точкой (float): Числа с десятичной точкой, например, 3.14, -0.5.

2. **Строки:**
   - Строки (str): Символьные последовательности, заключенные в кавычки, например, "Привет, мир!", 'Python'.

## Работа с числами
1. **Арифметические операции:**
   - Сложение `+`, вычитание `-`, умножение `*`, деление `/`, возведение в степень `**`, деление с остатком `%`.
        ```python
        a = 5 
        b = 2
        print(a + b)
        
        >>> 7
        ```
        
        ```python
        a = 5 
        b = 2
        print(a - b)
        
        >>> 3
        ```
        
        ```python
        a = 5 
        b = 2
        print(a * b)
        
        >>> 10
        ```
        
        ```python
        a = 5 
        b = 2
        print(a ** b)
        
        >>> 25
        ```
        
        ```python
        a = 5 
        b = 2
        print(a % b)
        
        >>> 1
        ```
     
## Операторы сравнения и логические операторы
1. **Операторы сравнения:**
   - `==` (равно), `!=` (не равно), `>` (больше), `<` (меньше).

2. **Логические операторы:**
   - `and` (логическое И), `or` (логическое ИЛИ), `not` (логическое НЕ).

3. **Приоритет операторов:**
   - У операторов есть приоритет: скобки `()` -> возведение в степень `**` -> умножение и деление `*`, `/`, `//` -> сложение и вычитание `+`, `-`.

## Операции со строками
1. **Конкатенация:**
   - Объединение строк с помощью оператора `+`.
    ```python
    first_name = 'Artyom'
    last_name = 'Troshkin'
    print(first_name + last_name)
    
    >>> ArtyomTroshkin
    ```

2. **Индексация:**
   - Получение символа по индексу с использованием квадратных скобок, например, `my_string[0]` вернет первый символ.
    ```python
    my_string = 'Test string'
    print(
        my_string[0]
    )
    
    >>> T
    ```

3. **Срезы:**
   - Получение подстроки с использованием срезов, например, `my_string[1:4]` вернет подстроку с 2-го по 4-й символ.

    ```python
    my_string = 'Test string'
    print(
        my_string[1:4]
    )
    
    >>> est
    ```

## Введение в списки
1. **Создание списков:**
   - Создание списка с помощью квадратных скобок, например, `my_list = [1, 2, 3]`.

2. **Индексация:**
   - Получение элемента списка по индексу, например, `my_list[0]` вернет первый элемент.
    ```python
    my_list = [1, 2, 3]
    print(my_list[0])
    
    >>> 1
    ```

3. **Изменение:**
   - Изменение элемента списка по индексу, например, `my_list[1] = 42`.
    ```python
    my_list = [1, 2, 3]
    my_list[1] = 42
    print(my_list)
    
    >>> [1, 42, 3]
    ```
   - Присоединение элементов в конец списка `.append()`
    ```python
    my_list = [1, 2, 3]
    my_list.append(5)
    print(my_list)
    
    >>> [1, 2, 3, 5]
    ```
   - Вставка элементов в список на определенную позицию `.insert()`
    ```python
    my_list = [1, 2, 3]
    my_list.insert(0, 15)
    print(my_list)
    
    >>> [15, 1, 2, 3]
    ```
   - Удаление элементов из списка `del`, `pop()`'
    ```python
    my_list = [1, 2, 3]
    del my_list[0]
    print(my_list)
    
    >>> [2, 3]
    ```
    ```python
    my_list = [1, 2, 3]
    deleted = my_list.pop(1)
    print(my_list)
    print(deleted)
    
    >>> [1, 3]
    >>> 2
    ```
   - Удаление элементов по значению `.remove()`
    ```python
    my_list = [1, 2, 3]
    my_list.remove(1)
    print(my_list)
    
    >>> [2, 3]
    ```
   - Постоянная сортировка списка методом `sort()`
    ```python
    my_list = [3, 1, 2]
    my_list.sort()
    print(my_list)
    
    >>> [1, 2, 3]
    ```
   - Временная сортировка списка функцией `sorted()`
   ```python
   my_list = [3, 1, 2]
   temporary_sort = sorted(my_list)
   print(temporary_sort)
   print(my_list)
   
   >>> [1, 2, 3]
   >>> [3, 1, 2]
   ```
   - Вывод списка в обратном порядке `.reverse()`
   ```python
   my_list = [1, 2, 3]
   my_list.reverse()
   print(my_list)
   
   >>> [3, 2, 1]
   ```
   - Определение длины списка `len()`
   ```python
   my_list = [1, 2, 3]
   print(len(my_list))
   
   >>> 3
   ```

## Введение в множества

   1. **Создание множеств:**
      - Создание множества с помощью фигурных скобок или функции `set()`, например, `my_set = {1, 2, 3}` или `my_set = set([1, 2, 3])`.

   2. **Добавление элементов:**
      - Добавление элемента в множество с помощью метода `.add()`, например, `my_set.add(4)`.
      ```python
      my_set = {1, 2, 3}
      my_set.add(4)
      print(my_set)
   
      >>>    {1, 2, 3, 4}
      ```
   
   3. **Удаление элементов:**
      - Удаление элемента из множества с помощью метода `.remove()` или `.discard()`, например, `my_set.remove(2)` или `my_set.discard(5)`
      - Если элемент не существует, `.remove()` вызовет ошибку, в то время как `.discard()` не вызовет ошибку.
      ```python
      my_set = {1, 2, 3, 4}
      my_set.remove(2)
      my_set.discard(5)
      print(my_set)
   
      >>>    {1, 3, 4}
      ```
   
   4. **Операции с множествами:**
      - Объединение множеств с помощью оператора `|` или метода `.union()`, например, `result_set = set1 | set2` или `result_set = set1.union(set2)`.
      - Пересечение множеств с помощью оператора `&` или метода `.intersection()`, например, `result_set = set1 & set2` или `result_set = set1.intersection(set2)`.
      - Разность множеств с помощью оператора - или метода `.difference()`, например, `result_set = set1 - set2` или `result_set = set1.difference(set2)`.
      - Симметрическая разность множеств с помощью оператора `^` или метода `.symmetric_difference()`, например, `result_set = set1 ^ set2` или `result_set = set1.symmetric_difference(set2)`.

   5. **Проверка на подмножество и надмножество:**
      - Проверка, является ли одно множество **подмножеством** другого с помощью метода `.issubset()`, например, `is_subset = set1.issubset(set2)`.
      - Проверка, является ли одно множество **надмножеством** другого с помощью метода `.issuperset()`, например, `is_superset = set1.issuperset(set2)`.

   6. **Копирование множества:**
      - Cоздание копии множества с помощью метода `.copy()`, например, `new_set = my_set.copy()`.

   7. **Определение размера множества:**
      - Определение количества элементов в множестве с помощью функции `len()`, например, `set_size = len(my_set)`.

   8. **Определение различных элементов:**
      - Получение списка уникальных элементов из итерируемого объекта с помощью функции `set()`, например, `unique_elements = set([1, 2, 2, 3, 3, 3])`.

## Введение в словари

1. **Создание словаря:**
   - Создание словаря с помощью фигурных скобок и пар "ключ: значение", например, `my_dict = {"name": "Анна", "age": 30}`.

2. **Доступ к элементам:**
   - Получение значения по ключу, например, `name = my_dict["name"]`.
   ```python
   my_dict = {"name": "Анна", "age": 30}
   name = my_dict["name"]
   print(name)
   
   >>> "Анна"
   ```

3. **Изменение элементов:**
   - Изменение значения по ключу, например, `my_dict["age"] = 31`.
   ```python
   my_dict = {"name": "Анна", "age": 30}
   my_dict["age"] = 31
   print(my_dict)
   
   >>> {"name": "Анна", "age": 31}
   ```
   
4. **Добавление элементов:**
   - Добавление новой пары "ключ: значение" в словарь, например, `my_dict["city"] = "Minsk"`.
   ```python
   my_dict = {"name": "Анна", "age": 30}
   my_dict["city"] = "Minsk"
   print(my_dict)
   
   >>> {"name": "Анна", "age": 30, "city": "Minsk"}
   ```
   
5. **Получение значения с указанием значения по умолчанию:**
   - Метод `.get(key, default)` позволяет получить значение по ключу, при этом можно указать значение по умолчанию, которое будет возвращено, если ключ не существует.
   ```python
   my_dict = {"name": "Анна", "age": 30}
   name = my_dict.get("name", "None")
   city = my_dict.get("city", "None")
   print(name)  # "Анна"
   print(city)  # "None"
   ```
   
6. **Получение всех ключей и значений:**
   - Методы `.keys(`) и `.values()` позволяют получить все ключи и значения из словаря соответственно.
   ```python
   my_dict = {"name": "Анна", "age": 30}
   keys = my_dict.keys()
   values = my_dict.values()
   print(keys)  # dict_keys(['name', 'age'])
   print(values)  # dict_values(['Анна', 30])
   ```
   
7. **Получение пар "ключ: значение" в виде кортежей:**
   - Метод `.items()` позволяет получить все пары "ключ: значение" в виде кортежей.
   ```python
   my_dict = {"name": "Анна", "age": 30}
   items = my_dict.items()
   print(items)  # dict_items([('name', 'Анна'), ('age', 30)])
   ```
   
8. **Обновление словаря:**
   - Метод `.update(dictionary`) позволяет обновить словарь, добавив элементы из другого словаря.
   ```python
   my_dict = {"name": "Анна", "age": 30}
   other_dict = {"city": "Москва", "gender": "женский"}
   my_dict.update(other_dict)
   print(my_dict)
   # {'name': 'Анна', 'age': 30, 'city': 'Москва', 'gender': 'женский'}
   ```
   
9. **Удаление и возврат значения по ключу:**
   - Метод `.pop(key)` удаляет элемент с указанным ключом из словаря и возвращает его значение.
   ```python
   my_dict = {"name": "Анна", "age": 30}
   age = my_dict.pop("age")
   print(age)  # 30
   ```

10. **Удаление элементов:**
    - Удаление элемента по ключу с помощью оператора `del`, например, `del my_dict["city"]`.
    ```python
    my_dict = {"name": "Анна", "age": 30, "city": "Москва"}
    del my_dict["city"]
    print(my_dict)
   
    >>> {"name": "Анна", "age": 30}
    ```

11. **Проверка наличия ключа:**
    - Проверка, существует ли ключ в словаре с помощью оператора `in`, например, `if "city" in my_dict:`.

12. **Итерация по словарю:**
    - Перебор всех ключей с помощью цикла `for`, например:
    ```python
    my_dict = {"name": "Анна", "age": 30}
    for key in my_dict:
        print(key, my_dict[key])
   
    >>> имя Анна
    >>> возраст 30
    ```
   
13. **Копирование словаря:**
    - Создание копии словаря с помощью метода `.copy()`, например, `new_dict = my_dict.copy()`.

14. **Определение размера словаря:**
    - Определение количества пар "ключ: значение" в словаре с помощью функции `len()`, например, `dict_size = len(my_dict)`.

## Литература:
- [Python: коллекции](https://habr.com/ru/articles/319164/)
- [Sequence Types — list, tuple, range](https://docs.python.org/3/library/stdtypes.html?highlight=list#sequence-types-list-tuple-range)
- [Boolean Operations — and, or, not](https://docs.python.org/3/library/stdtypes.html?highlight=list#boolean-operations-and-or-not)
- [Comparison](https://docs.python.org/3/library/stdtypes.html?highlight=list#comparisons) 
- [Boolean Type - bool](https://docs.python.org/3/library/stdtypes.html?highlight=list#boolean-type-bool)
- [Set Types — set, frozenset](https://docs.python.org/3/library/stdtypes.html?highlight=list#set-types-set-frozenset)
- [Mapping Types — dict](https://docs.python.org/3/library/stdtypes.html?highlight=list#mapping-types-dict)
- [Built-in Types](https://docs.python.org/3/library/stdtypes.html)