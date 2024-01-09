# Дата и время

В зависимости от задачи мы можем создать объекты нескольких типов:

* дату ``from datetime import date``,
* время ``from datetime import time``,
* время и дату ``from datetime import datetime``.

### Создаем дату

``date(<год>, <месяц>, <число>)``

```
from datetime import date

date_one = date(1815, 12, 12) # 12 декабря 1815

print(date_one)

# Выведет 1815-12-12
```

### Создаем время
При создании времени мы указываем часы, минуты и секунды:

``time(<часы>, <минуты>, <секунды>)``
```
from datetime import time

time_one = time(16, 20, 00) # 16 часов 20 минут

print(time_one)

# Выведет 16:20:00
```

### Создаем время с датой
При создании времени вместе с датой мы указываем всё вместе, начиная с года и заканчивая секундами, а то, что мы не укажем, считается равным нулю:

``datetime( <год>, <месяц>, <число>, <часы>, <минуты>, <секунды>)``

```
from datetime import datetime

datetime_one = datetime(1986, 4, 26, 1, 23, 47) # 26 апреля 1986 01:23:47

print(datetime_one)

# Выведет 1986-04-26 01:23:47
```

### Работа с объектом даты
Чтобы работать с датой, есть специальные атрибуты, например:

<table>
<tr><td>thedate.year</td><td>год</td></tr>
<tr><td>thedate.month</td><td>месяц</td></tr>
<tr><td>thedate.day</td><td>день</td></tr>
<tr><td>thedate.hour</td><td>час</td></tr>
<tr><td>thedate.minute</td><td>минута</td></tr>
<tr><td>thedate.second</td><td>секунда</td></tr>
</table>

```
from datetime import datetime

thedate = datetime(1986, 4, 26, 1, 23, 47) # 26 апреля 1986 01:23:47

print("Год", thedate.year)
print("Месяц", thedate.month)
print("День", thedate.day)
print("Час", thedate.hour)
print("Минута", thedate.minute)
print("Секунда", thedate.second)```

# Выведет

Год 1986
Месяц 4
День 26
Час 1
Минута 23
Секунда 47
```

### Работа с текущей датой

``datetime.now()``

### Получение даты из строки
Поскольку не все форматы файлов и данных поддерживают дату и дата часто передается просто в виде строки, часто вы будете получать дату из строк. Для этого есть метод ``fromisoformat(<строка даты>)``, который позволяет вытащить дату в 
date, time, datetime.

```
from datetime import date

thedate = date.fromisoformat("2021-05-04")

print(thedate.year)
print(thedate.month)
print(thedate.day)

# Выведет:

2021
5
4
```

### Форматирование даты
Если вам не нравится доставать время и дату по кусочкам, можно форматировать ее с помощью метода ``strftime()`` (от string format time) и специальной строки-шаблона, например:

```
from datetime import date

thedate = date(1970, 1, 5)

date_formatted = thedate.strftime("%d %B %Y ") # День Месяц Год

print(date_formatted)

# Выведет 05 January 1970
```

Вот какие буквы вы можете использовать:

<table>
<tr><td>%y</td><td>Год, короткая версия</td></tr>
<tr><td>%Y</td><td> полная версия</td></tr>
<tr><td>%m</td><td>Месяц номером</td></tr>
<tr><td>%B</td><td>Месяц словом</td></tr>
<tr><td>%d</td><td>День, от 01 до 31</td></tr>
<tr><td>%H</td><td>Час, от 00 до 23</td></tr>
<tr><td>%M</td><td>Минуты, от 00 до 59</td></tr>
<tr><td>%S</td><td>Секунды, от 00 до 59</td></tr>
</table>

### Вычисление разницы между датами
Часто в приложениях можно встретить уведомления типа «отправлено 2 часа назад», или «до вашего рейса осталось 15 минут», или «вот ваши фотографии год назад». Высчитывать промежуток между двумя датами можно с помощью ``timedelta``. Например, можно узнать, сколько времени прошло между 7:10 и 7:30:

```
from datetime import date

# Задает первую дату
time_one = date(2020, 10, 1)
# Задает вторую дату
time_two = date(2020, 10, 2)

# Вычисляет расстояние в формате timedelta
delta = time_two - time_one

print(delta)

# Выведет 1 day, 0:00:00
```
Timedelta можно считать для типов date и datetime.
