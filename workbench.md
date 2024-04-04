# Workbench

**Подключение к локальному серверу**
Если сервер MySQL запущен на том же хосте, что и Workbench то на приветсвенном экране будет показан адрес сервера (раздел MySQL Connections)

<img src="assets/workbench_main_screen.png">

Кликните на сервере для подключения.\
Появится окно для ввода пароля, введите его.\
Откроется основное окно Workbench для работы с сервером:


**Подключение к удалённому серверу**
Меню Database > Connect to database (<kbd>Ctrl</kbd>+<kbd>U</kbd>).\
Необходимо задать:
- Hostname — IP адрес или имя сервера;
- Port — порт, если не по умолчанию;
- Username — имя пользователя;
- Password — пароль.

<img src="assets/workbench_connect.png">

**Основное окно**

<img src="assets/workbench_server_status.png">

В левой части окна (**Administration**) находятся панели управления (Managment, Instance, Performance). 

В первой влкладке 
(**Administration - Server Ststus**) открыт раздел Server Status. Он показывает основные сведения о работе сервера, к которому сейчас открыто соединение.\

Вторая вкладка **Query 7** — окно запросов. В нём записываются SQL запросы 


**Базы данных и окно запросов**
Раздел **Schemas** (левая часть окна) показывает существующие БД, их таблицы, представления и т.д. На рис. ниже видна БД `Course`.

<img src="assets/workbecn_query_schemas.png">

<br>

**Выполнение SQL команд из файла**\
Меню Server > Data Import > Выбрать файл.

или

Открыть вкладку с запросами (Queries), нажмите на кнопку открытия файла (значёк - папка), выерите файл, не выделяйте текст, нажниме на кнопку выполнения запроса (молния). 


Выполнить sql файл, который ссылается на другие sql и dump файлы:
Меню File >  Run SQL Script

Workbench запустит консольный клиент mysql для выполнения файла и выполнит его.


См. также выполнение sql файла (со ссылками на другие файлы) в [консольном клиенте MySQL](https://github.com/VetrovSV/DataBases/blob/main/MySQL.md#%D1%80%D0%B5%D0%B7%D0%B5%D1%80%D0%B2%D0%BD%D0%BE%D0%B5-%D0%BA%D0%BE%D0%BF%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D1%8D%D0%BA%D1%81%D0%BF%D0%BE%D1%80%D1%82-%D0%B8-%D0%B8%D0%BC%D0%BF%D0%BE%D1%80%D1%82)