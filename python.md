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



#### Запросы
```python
# объект для совершения запросов к БД
cursor = connection.cursor()

# выполнение запроса
cursor.execute('SELECT * FROM Users')
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
cursor.execute("SELECT name FROM sqlite_master WHERE type='table';")
print(cursor.fetchall())
```

### todo: ORM

## См. также
- клиентское приложение для СУБД DBeaver
- Работа с СУБД в Java: https://github.com/ivtipm/BigDataLanguages/tree/main/Java/DataBase