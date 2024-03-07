# MySQL

<img src="https://upload.wikimedia.org/wikipedia/ru/thumb/d/d3/Mysql.png/310px-Mysql.png" width=200>

**MySQL** - реляционная клиент-серверная СУБД. Распространяется под свободной (GPL) и коммерческой лицензией, разрабатывается Oracle.

В дистрибутив входит серверное приложение и клиентское приложение MySQL Workbench.

Входит в состав популярных сборок сервером для веб-разработки: Денвер, WAMP, LAMP, XAMPP и др.

Реализована для большинства платформ включая Windows, Linux, MacOS.

Имеет API для популярных языков включая Python, C++, C, Java, C#.


### Установка

[Последняя версия (на март 2024) - 8.3.0](https://www.mysql.com/downloads/).
Версия MySQL Community (GPL) бесплатна.


**Ubuntu**
```bash
# устанвока
sudo apt install mysql-server

# запуск сервиса
sudo systemctl start mysql.service

# установка клиентского приложения 
sudo apt install mysql-workbench
```