# Тема 3: Введение в условные операторы

Условные операторы в Python позволяют выполнять различные блоки кода в зависимости от выполнения определенных условий. Условие представляет собой выражение, результат которого может быть истинным (`True`) или ложным (`False`).

### Оператор if

1. **Структура оператора if:**
   - Оператор `if` используется для выполнения блока кода, если заданное условие истинно.
   - Синтаксис оператора if:
   
   ```python
   if <условие>:
       # Блок кода, выполняемый, если условие истинно
   ```
   
2. **Примеры оператора if:**
   - Проверка числа на четность.
    ```python
    num = 10
    if num % 2 == 0:
        print("Число четное")
    ```
   
### Операторы elif и else: множественные условия

1. **Оператор elif:**
   - Оператор `elif` используется, чтобы проверить дополнительные условия, если предыдущие условия были ложными.
   - Синтаксис оператора `elif`:
   ```python
   if <условие1>:
       # Блок кода, выполняемый, если условие1 True
   elif <условие2>:
       # Блок кода, выполняемый, если условие2 True
   else:
       # Блок кода, выполняемый, если ни одно из условий не True
   ```
   - Пример проверки положительных и отрицательных чисел:
   ```python
   number = int(input("Введите число: "))
   
   if number > 0:
       print("Число положительное")
   elif number < 0:
       print("Число отрицательное")
   else:
       print("Число равно нулю")
   ```
   
### Логические операторы

1. **Оператор `and`:**
   - Оператор `and` возвращает `True`, если оба операнда являются истинными. В противном случае он возвращает `False`.
   ```python
   if <условие1> and <условие2>:
       # Блок кода, выполняемый, если оба условия истинны
   ```

2. **Оператор `or`**
   - Оператор `or` возвращает `True`, если хотя бы один из операндов является истинным. Если оба операнда ложны, он возвращает `False`.
   ```python
   if <условие1> or <условие2>:
       # Блок кода, выполняемый, если условие ложно
   ```
   
3. **Оператор `not`:**
   - Оператор `not` используется для инверсии логического значения. Если условие истинно, то `not` условие будет ложным, и наоборот.
   ```python
   if not условие:
       # Блок кода, выполняемый, если условие ложно
   ```
   
### Вложенные условные операторы
   - Вложенные условные операторы позволяют вам включать один условный оператор внутри другого. Это полезно для обработки более сложных сценариев.
   ```python
   if <условие1>:
       if <условие2>:
           # Блок кода, выполняемый, если оба условия истинны
       else:
           # Блок кода, выполняемый, если только условие1 истинно
   else:
       # Блок кода, выполняемый, если условие1 ложно
   ```

### Тернарный оператор
   - Тернарный оператор позволяет сократить условное выражение до одной строки. Он имеет следующий синтаксис:
   ```python
   значение_if_истинно if условие else значение_if_ложно
   ```
   - Пример: 
   ```python
   number = 5
   result = "Четное" if number % 2 == 0 else "Нечетное"
   print(result)
   ```

### Сравнение строк
   - Строки в Python можно сравнивать на равенство и с использованием лексикографического порядка. Операторы сравнения строк возвращают логические значения `True` или `False`.
   ```python
   str_1 = "apple"
   str_2 = "banana"
   
   if str_1 == str_2:
       print("Строки равны")
   else:
       print("Строки не равны")
   
   if str_1 < str_2:
       print("str_1 идет раньше по алфавиту")
   else:
       print("str_2 идет раньше по алфавиту")
   ```

## Литература
- [if Statements](https://docs.python.org/3/tutorial/controlflow.html#if-statements)