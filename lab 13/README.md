# Лабораторна робота №11: Робота з Масивами Чисел в Python

### Мета роботи:
#### Навчитися різним методам роботи з числовими масивами в Python.

### Очікуваний результат:
# Отримати практичні навички виконання задач, пов'язаних з масивами чисел.

### Опис завдання:
#### У цій лабораторній роботі потрібно було виконати кілька завдань. Для кожного завдання слід написати функцію, яка вирішує конкретну задачу, пов'язану з масивами чисел. Наприклад: обчислення суми квадратів чисел, усереднення, сортування за частотою елементів тощо.

### Виконання роботи:
#### Структура проекту:
##### Код розділено на функції, кожна з яких вирішує окрему задачу і має відповідну назву.

#### Опис файлів:
##### student_main.py:
# Містить Python-код із функціями для вирішення завдань.

##### README.md:
# Описує структуру проекту, призначення кожного файлу, а також основні функції та методи з поясненням їх роботи.

### Опис основних функцій та методів з поясненням їх роботи:

#### interpolate_missing(numb):
##### Опис:
# Функція виконує інтерполяцію відсутніх значень у масиві.

def interpolate_missing(numb):
    interpolated = []
    for i, num in enumerate(numb):
        if num is None:
            left_index = i - 1
            right_index = i + 1
            left_value = None
            right_value = None
            while left_index >= 0:
                if numb[left_index] is not None:
                    left_value = numb[left_index]
                    break
                left_index -= 1
            while right_index < len(numb):
                if numb[right_index] is not None:
                    right_value = numb[right_index]
                    break
                right_index += 1

            if left_value is not None and right_value is not None:
                distance = right_index - left_index
                interpolated_value = left_value + ((right_value - left_value) / distance) * (i - left_index)
                interpolated.append(round(interpolated_value))
            elif left_value is not None:
                interpolated.append(left_value)
            elif right_value is not None:
                interpolated.append(right_value)
            else:
                interpolated.append(None)
        else:
            interpolated.append(num)
    return interpolated

#### fibonacci(n):
##### Опис:
# Генерує перші n чисел Фібоначчі.

def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b

#### process_batches(nums, batch_size):
##### Опис:
# Обробляє масив чисел по батчах заданого розміру та повертає максимальне число кожного батча.

def process_batches(nums, batch_size):
    return [max(nums[i:i + batch_size]) for i in range(0, len(nums), batch_size)]

#### encode_string(s):
##### Опис:
# Кодує рядок за допомогою підрахунку кількості повторюваних символів.

def encode_string(s):
    encoded = ''
    count = 1
    for i in range(1, len(s)):
        if s[i] == s[i - 1]:
            count += 1
        else:
            encoded += str(count) + s[i - 1]
            count = 1
    encoded += str(count) + s[-1]
    return encoded

#### decode_string(s):
##### Опис:
# Декодує закодований рядок, відновлюючи вихідний рядок.

def decode_string(s):
    dec = ''
    i = 0
    while i < len(s):
        if s[i].isdigit():
            count = int(s[i])
            dec += s[i + 1] * count
            i += 2
        else:
            dec += s[i]
            i += 1
    return dec

#### rotate_matrix(matrix):
##### Опис:
# Виконує обертання матриці на 90 градусів за годинниковою стрілкою.

def rotate_matrix(matrix):
    return [list(row) for row in zip(*matrix[::-1])]

#### regex_search(str, pat):
##### Опис:
# Виконує пошук рядків, що відповідають заданому регулярному виразу.

import re

def regex_search(str, pat):
    return [string for string in str if re.search(pat, string)]

#### merge_sorted_arrays(arr1, arr2):
##### Опис:
# Об'єднує два відсортованих масиви в один відсортований масив.

def merge_sorted_arrays(arr1, arr2):
    merged = []
    i = j = 0
    while i < len(arr1) and j < len(arr2):
        if arr1[i] < arr2[j]:
            merged.append(arr1[i])
            i += 1
        else:
            merged.append(arr2[j])
            j += 1
    merged.extend(arr1[i:])
    merged.extend(arr2[j:])
    return merged

#### is_prime(num):
##### Опис:
# Перевіряє, чи є задане число простим.

def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            return False
    return True

#### group_by_key(data, key):
##### Опис:
# Групує елементи словника за заданим ключем.

def group_by_key(data, key):
    grouped = {}
    for item in data:
        grouped.setdefault(item[key], []).append(item['value'])
    return grouped

#### remove_outliers(list):
##### Опис:
# Видаляє виброси з масиву чисел.

import numpy as np

def remove_outliers(list):
    mean = np.mean(list)
    std_dev = np.std(list)
    z_scores = [(x - mean) / std_dev for x in list]
    threshold = 2

    return [x for x, z in zip(list, z_scores) if abs(z) <= threshold]

### Результати:
#### Виведення результатів роботи кожної функції наведено у вигляді рядків, де кожен рядок відповідає певній функції.

### Висновки:
#### Мета роботи досягнута: були розглянуті та реалізовані різні методи обробки числових масивів у Python, а також набуті навички роботи з ними.

### Інструкції з запуску:
#### Відкрийте файл будь-яким зручним для вас способом, де є встановлений інтерпретатор Python. Додайте необхідні виведення, наведені у файлі README.md. Після цього запустіть файл для отримання необхідних результатів.

