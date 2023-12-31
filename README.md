# Подсчет средней зарплаты языков программирования с HH.ru и SuperJob.ru

Эта программа позволяет вычислить среднюю зарплату для различных языков программирования, используя данные с популярных сайтов вакансий [HH.ru](https://hh.ru/) и [superjob.ru](https://www.superjob.ru/). Она предоставляет полезную информацию о средних зарплатах в программировании и может быть полезна для разработчиков и IT-специалистов

В проекте реализованы 3 отдельных программы:

`fetch_hh`  - программа позволяет использовать данные HH.ru для подсчета средней ЗП по языкам программирования и представления в табличном виде.

`fetch_sj` - программа позволяет использовать данные SuperJob.ru для подсчета средней ЗП по языкам программирования и представления в табличном виде.

`sj_and_hh_statistics_table` - программа позволяет использовать данные HH.ru и SuperJob.ru для подсчета средней ЗП по языкам программирования и представления в табличном виде.


### Как установить

Для использования программ `fetch_sj` и `sj_and_hh_statistics_table`, изначально необходимо зарегистрировать приложение.

`SJ_APP_ID` - секретный ключ (Secret key) вашего приложения для взаимодействия с api SuperJob.ru

Для каждого запроса необходимо в заголовке X-Api-App-Id передавать секретный ключ (Secret key) вашего приложения. 

Пример ключа: `v3.r.119807100.2229e78192ec711add83435b5c68f485b4e613fa.de6ae7869055b4248d3156c0c98ab0e694`

[Ссылка с инструкциями для регистрации приложения](https://api.superjob.ru/)

Полученный токен необходимо разместить в файле `.env`, переменная  `APP_ID`


Python3 должен быть уже установлен. 
Затем используйте `pip` (или `pip3`, есть конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```

### Запуск скриптов

```
python fetch_hh -pl/--program_language [Список языков программирования]
```
Параметр Список языков программирования указывается  через пробелы при передаче аргументов командной строки.

```
python fetch_hh -pl python java
```

По умолчанию программа будет собирать статистику для языков программирования, заданных в файле languages.py переменная languages.

```
python fetch_sj -pl/--program_language [Список языков программирования]
```
Параметр Список языков программирования указывается  через пробелы при передаче аргументов командной строки.

```
python fetch_sj -pl python java
```

По умолчанию программа будет собирать статистику для языков программирования, заданных в файле languages.py переменная languages.

