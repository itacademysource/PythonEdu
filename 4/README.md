# Тема 4: Циклы

Циклы в Python предоставляют механизм для выполнения одного и того же блока кода несколько раз. Они могут быть полезными при обработке повторяющихся задач и данных.

### **Цикл `for`**

1. **Структура цикла `for`:**
   - Цикл `for` используется для итерации по итерируемому объекту, такому как список, кортеж или строка, и выполняет блок кода для каждого элемента в объекте.
   - Синтаксис цикла `for`:
   
   ```python
   for <элемент> in <итерируемый_объект>:
       # Блок кода, выполняемый для каждого элемента
   ```

2. **Примеры цикла `for`:**
   - Итерация по списку чисел и вывод их на экран.
   ```python
   numbers = [1, 2, 3, 4, 5]
   for number in numbers:
       print(number)
   
   >>> 1
       2
       3
       4
       5
   ```
   - Итерация по строке и подсчет букв "e".
   ```python
   string = "some text"
   count = 0
   for symbol in string:
       if symbol == "e":
           count += 1
   print(count)
   
   >>> 2
   ```
   
### **Цикл `while`**
1. **Структура цикла `while`:**
   - Цикл `while` выполняет блок кода, пока указанное условие истинно.
   - Синтаксис цикла `while`:
   ```python
   while <условие>:
       # Блок кода, выполняемый, пока условие истинно
   ```
   
2. **Пример цикла `while`:**
   - Вычисление факториала числа.
   ```python
   number = 5
   factorial = 1
   while number > 0:
       factorial *= number
       number -= 1
   print(factorial)
   ```
   
### **Операторы `break` и `continue`**
1. **Оператор `break`:**
   - Оператор `break` используется для прерывания выполнения цикла и выхода из него, даже если условие цикла все еще истинно.
   ```python
   for i in range(1, 11):
       if i == 5:
           break  # Прерывает цикл, если i становится равным 5
       print(i)
   
   >>> 1
       2
       3
       4
   ```
   
2. **Оператор `continue`:**
   - Оператор `continue` используется для перехода к следующей итерации цикла, игнорируя оставшуюся часть текущей итерации.
   ```python
   for i in range(1, 11):
       if i % 2 == 0:
           continue  # Пропускает четные числа и переходит к следующей итерации
       print(i)
   
   >>> 1
       3
       5
       7
       9
   ```


### Инструкция `else` в циклах
1. **Инструкция `else` в циклах:**
   - Вы можете использовать инструкцию `else` после цикла для выполнения блока кода после завершения цикла, если цикл завершился нормально (без прерывания оператором `break`).

   ```python
   numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
   for num in numbers:
       if num == 0:
           print("Найден ноль")
           break
   else:
       print("Ноль не найден")
   
   >>> Ноль не найден
   ```

## Литература
- [for Statements](https://docs.python.org/3/tutorial/controlflow.html#for-statements)
- [The while Statements](https://docs.python.org/3/reference/compound_stmts.html#the-while-statement)
- [break and continue Statements, and else Clauses on Loops](https://docs.python.org/3/tutorial/controlflow.html#break-and-continue-statements-and-else-clauses-on-loops)
- [pass Statements](https://docs.python.org/3/tutorial/controlflow.html#pass-statements)