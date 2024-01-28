# Python и СУБД
## SQLite
Пекет `sqlite3` уже входит в стандартную библиотеку Python.

Документация: https://docs.python.org/3/library/sqlite3.html

#### Подключение к БД
```python
import sqlite3

# Создаем подключение к БД, если файла БД ('my_database.db')  не существует, то он будет создан
connection = sqlite3.connect('my_database.db')

connection.close()
```



#### Запросы select
```python
# объект для совершения запросов к БД
cursor = connection.cursor()

# выполнение запроса
cursor.execute('select * from Users')
# получение результата запроса в виде списка
users = cursor.fetchall()

# вывод всех строк из результата запроса
for user in users:
    # user -- кортеж (tuple)
    print(user)
    # типы элементов кортежа соответствуют типам данных каждого поля в таблице
```

Для получения перечня всех таблиц тоже используется запрос select к служебной таблице
```python
cursor = conn.cursor()
cursor.execute("select name from sqlite_master WHERE type='table';")
print(cursor.fetchall())
```

Запрос с параметрами удобно делать через форматную строку, например:
```python
email = input()
cursor.execute(f'select email, login from Users where email={"email"}')
```

Длинные запросы стоит разбивать на несколько строк для лучшей читаемости:
```python
min_age = int(input())
cursor.execute(f"""select email, login, age 
                   from Users 
                   where age>{min_age} 
                   order by age asc""")
```

Методы получения данных
- `fetchone()` — получить первый результат выполнения запроса,
- `fetchmany(n)` — получить n результатов запроса,
- `fetchall()` — получить все результаты запроса.

#### Модификация данных
todo
См. также SQL-инъекции

#### Работа с таблицами
todo

#### Исключения
todo

#### ...


### todo: ORM

## См. также
- клиентское приложение для СУБД DBeaver
- Работа с СУБД в Java: https://github.com/ivtipm/BigDataLanguages/tree/main/Java/DataBase


# Ссылки
- https://habr.com/ru/articles/754400/
- Документация sqlite3: https://docs.python.org/3/library/sqlite3.html