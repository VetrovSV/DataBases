# Python и СУБД
## SQLite
Пекет `sqlite3` уже входит в стандартную библиотеку Python.


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
# получение всех данных
users = cursor.fetchall()

# вывод всех строк из рещзультата запроса
for user in users:
  print(user)
```
### todo: ORM

## См. также
- клиентское приложение для СУБД DBeaver
- Работа с СУБД в Java: https://github.com/ivtipm/BigDataLanguages/tree/main/Java/DataBase