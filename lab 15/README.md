# Лабораторна робота №15: Робота з текстом та числовими даними в Python

### Мета роботи:
#### Навчитися різним методам обробки текстових та числових даних в Python.

#### Очікуваний результат:
# Отримати практичні навички виконання задач, пов'язаних з обробкою текстових та числових даних.

### Опис завдання:
#### У цій лабораторній роботі потрібно було виконати кілька завдань. Для кожного завдання слід написати функцію, яка вирішує конкретну задачу, пов'язану з обробкою текстових та числових даних. Наприклад: очищення даних, фільтрація email-адрес, нормалізація чисел тощо.

### Виконання роботи:
#### Структура проекту:
##### Код розділено на функції, кожна з яких вирішує окрему задачу і має відповідну назву, наприклад: clean_data, filter_emails, extract_keywords і т.д.

#### Опис файлів:
##### main.py:
# Містить Python-код із функціями для вирішення завдань.

##### README.md:
# Описує структуру проекту, призначення кожного файлу, а також основні функції та методи з поясненням їх роботи.

### Опис основних функцій та методів з поясненням їх роботи:
#### clean_data(data):
# Очищає текстові дані, видаляючи зайві пробіли та переводячи текст у нижній регістр.

##### Приклад використання:
# ```python
# data = " Apple,  Banana , orange "
# print(clean_data(data))  # Виведе: ['apple', 'banana', 'orange']
# ```

#### filter_emails(emails_string):
# Фільтрує валідні email-адреси з рядка.

##### Приклад використання:
# ```python
# emails = "mail us test@example.com and invalid-email.com.djwd with example@test.co"
# print(filter_emails(emails))  # Виведе: ['test@example.com', 'example@test.co']
# ```

#### extract_keywords(words, length):
# Витягує слова, довжина яких перевищує задане значення.

##### Приклад використання:
# ```python
# words = "apple pear banana kiwi"
# print(extract_keywords(words, 4))  # Виведе: ['apple', 'banana']
# ```

#### process_text(text):
# Обробляє текст, видаляючи пунктуацію та приводячи до нижнього регістру.

##### Приклад використання:
# ```python
# texts = "Hello! , Yes? , No. , "
# print(process_text(texts))  # Виведе: ['hello', 'yes', 'no']
# ```

#### normalize_data(numbers):
# Нормалізує числові дані до діапазону [0, 1].

##### Приклад використання:
# ```python
# numbers = "10, 20, 30, 40, 50"
# print(normalize_data(numbers))  # Виведе: [0.2, 0.4, 0.6, 0.8, 1.0]
# ```

#### concatenate_strings(data, separator):
# Об'єднує рядки з використанням заданого роздільника.

##### Приклад використання:
# ```python
# data_to_concatenate = "Hello, World!, How, are, you?"
# separator = ","
# print(concatenate_strings(data_to_concatenate, separator))  # Виведе: 'Hello World! How are you?'
# ```

#### sum_numeric_strings(numbers):
# Обчислює суму чисел у рядку.

##### Приклад використання:
# ```python
# numeric_strings = "10, 20, abc, 30, def, 40"
# print(sum_numeric_strings(numeric_strings))  # Виведе: 100
# ```

#### filter_numbers(input_string, threshold):
# Фільтрує числа у рядку, залишаючи лише ті, що більше заданого порогу.

##### Приклад використання:
# ```python
# numbers_to_filter = "10, 20, abc, 30, def, 40"
# threshold = 25
# print(filter_numbers(numbers_to_filter, threshold))  # Виведе: [30, 40]
# ```

#### map_to_squares(numbers):
# Повертає список квадратів чисел.

##### Приклад використання:
# ```python
# numbers_to_square = "1, 2, 3, 4, 5"
# print(map_to_squares(numbers_to_square))  # Виведе: [1, 4, 9, 16, 25]
# ```

#### reverse_strings(words):
# Повертає список рядків у зворотному порядку.

##### Приклад використання:
# ```python
# strings_to_reverse = "apple, banana, orange, PEAR, kiwi"
# print(reverse_strings(strings_to_reverse))  # Виведе: ['elppa', 'ananab', 'egnaro', 'RAEP', 'iwik']
# ```

### Результати:
#### Виведення результатів роботи кожної функції наведено у вигляді рядків, де кожен рядок відповідає певній функції: 1-й рядок - clean_data, 2-й рядок - filter_emails і т.д.

### Висновки:
#### Мета роботи досягнута: були розглянуті та реалізовані різні методи обробки текстових та числових даних у Python, а також набуті навички роботи з ними.

### Інструкції з запуску:
#### Відкрийте файл будь-яким зручним для вас способом, де є встановлений компілятор Python. Додайте необхідні виведення, наведені у файлі README.md. Після цього запустіть файл для отримання необхідних результатів.
![image](https://github.com/DanilSobko/Python/assets/144261572/ae279d1f-2c63-480e-9ef0-014d4869cb3f)

