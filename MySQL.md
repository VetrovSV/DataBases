# MySQL

<img src="https://upload.wikimedia.org/wikipedia/ru/thumb/d/d3/Mysql.png/310px-Mysql.png" width=200>

**MySQL** - реляционная клиент-серверная СУБД. Распространяется под свободной (GPL) и коммерческой лицензией, разрабатывается Oracle.

В дистрибутив входит серверное приложение и клиентское приложение MySQL Workbench.

Входит в состав популярных сборок сервером для веб-разработки: Денвер, WAMP, LAMP, XAMPP и др.

Реализована для большинства платформ включая Windows, Linux, MacOS.

Имеет API для популярных языков включая Python, C++, C, Java, C#.

Информация о MySQL на сайте https://stackshare.io/mysql.


### Установка

[Последняя версия (на март 2024) - 8.3.0](https://www.mysql.com/downloads/).
Версия MySQL Community (GPL) бесплатна.


**Ubuntu**
```bash
# устанвока
sudo apt install mysql-server

# запуск сервиса
sudo systemctl start mysql.service
# проверить состояние сервиса
sudo systemctl status mysql.service


# установка клиентского приложения 
sudo snap install mysql-workbench-community
```

**Windows**
...

Подробнее об установке: https://www.mysqltutorial.org/getting-started-with-mysql/install-mysql/ или https://dev.mysql.com/doc/refman/8.3/en/installing.html 



**См. также образ Docker**




### Начальная настройка

#### Задание пароля доступа к серверу СУБД
##### Linux

**Запустить консольное клиентское приложение от имени суперспользователя:**
```bash
sudo mysql
```
Запуск от имени суперпользователя позволит настроить сервер без ввода пароля администратора пользователя.


**Задать имя суперпользователя сервера root**
```sql
ALTER USER root@localhost 
IDENTIFIED WITH mysql_native_password  
BY '<YOUR_PASSWORD>';
```
где `<YOUR_PASSWORD>` обозначает задаваемый пароль.  Важно не потерять этот пароль.

Аналогично можно задать имена для других пользователей.


Далее можно запускать клиентское приложение mysql так:
```bash
mysql -u root -p
```

**Дополнительно**
Просмотреть список пользователей через выполнение запроса к таблице user служебной базы данных mysql:
```sql
select user from mysql.user;
```

Показать все существующие БД можно так:
```sql
show databases;
```

Выход из консольного клиента:
```text
exit;
```

Запустить скрипт безопасности для завершения настройки
```bash
sudo mysql_secure_installation
```
Скрипт будет выполняться в режиме мастера, нужно ответить на вопросы о настройке безопасности: удалить анонимных пользователей, запретить пользователю root подключаться по сети, удалить тестовую БД test

См. также `mysqladmin` - клиентское приложение MySQL для администрирования сервера.