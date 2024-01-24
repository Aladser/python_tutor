# Работа со строками

## Функция print()

+ Многострочные строки

Чтобы разместить строку на нескольких строчках, используются тройные одинарные (''') или тройные двойные (""") кавычки:

```
print('''Однажды по дорожке
Я шел к себе домой 
Смотрю и вижу: кошки
Сидят ко мне спиной
''')
```

+ f-строки

```
a = 1
print(f"число {a}")
```
## Функция ввода input()

Функция ``input()`` записывает введенное пользователем значение в переменную.

## Сепараторы

Можем переопределить разделитель — сепаратор (separator). Он указывается в круглых скобках функции print через запятую после перечисления всех выводимых значений:

```
print(данные, sep="здесь_указывается_разделитель")
```

## Конец строки

По умолчанию в конце вывода добавляется символ переноса строки (\n). Однако мы можем переопределить конец строки с помощью end. Чаще всего это делается для того, чтобы вывести несколько сообщений в одну строку:

```
print("Однажды ", end="")
print("По дорожке ", end="")
print("Я шел", end="")
print("К себе домой", end="")
```
## Кавычки и экранирование

+ Альтернативные кавычки.

Внутри одинарных кавычек используются двойные:

```
print('Введите в терминале "да" или "нет" ')
```

Внутри двойных кавычек — одинарные:

```
print("Введите в терминале 'да' или 'нет' ")
```

+ Тройные кавычки:

```
print("""Введите в терминале "да" или "нет" """)
```

+ Экранирование.

Экранирование символов — замена в тексте управляющих символов на соответствующие текстовые подстановки. В Python для этого используется обратный слеш (backslash).

Внутри двойных кавычек используются двойные с экранированием:

```
print("Введите в терминале \"да\" или \"нет\" ")
```

Внутри одинарных кавычек используются одинарные с экранированием:

```
print('Введите в терминале \'да\' или \'нет\' ')
```

# Функции для работы со строками

``len`` - длина строки

``str`` - преобразование в строку

## Срезы (slices)

&emsp;Срез (slice) — извлечение из данной строки одного символа или некоторого фрагмента подстроки или подпоследовательности.

Формы срезов. 
* **Взятие одного символа строки S[i]**

![Таблица срезов](/images/img1.png)

* **Срез с двумя параметрами: S[a:b]** 
  
возвращает подстроку из `b - a` символов, начиная с символа c индексом a, то есть до символа с индексом b, не включая его. Если опустить второй параметр (но поставить двоеточие), то срез берется до конца строки.

* **Срез с тремя параметрами S[a:b:d]** 
  
третий параметр задает шаг, как в случае с функцией range, то есть будут взяты символы с индексами a, a + d, a + 2 * d и т. д. При задании значения третьего параметра, равному 2, в срез попадет кажый второй символ, а если взять значение среза, равное -1, то символы будут идти в обратном порядке. Например, можно перевернуть строку срезом S[::-1].

## Методы

+ ``find, rfind`` - find возвращает индекс первого вхождения подстроки, rfind - последнее вхождение. Если же подстрока не найдена, то метод возвращает значение -1. Если вызвать метод find с тремя параметрами S.find(T, a, b), то поиск будет осуществляться в срезе S[a:b]. Если указать только два параметра S.find(T, a), то поиск будет осуществляться в срезе S[a:]. Метод S.find(T, a, b) возращает индекс в строке S, а не индекс относительно среза.
+ ``replace`` - Метод replace заменяет все вхождения одной строки на другую. Формат: S.replace(old, new) — заменить в строке S все вхождения подстроки old на подстроку new. Если методу replace задать еще один параметр: S.replace(old, new, count), то заменены будут не больше, чем первые count из них.
+ ``count`` - подсчитывает количество вхождений одной строки в другую строку. Простейшая форма вызова S.count(T)  возвращает число вхождений строки T внутри строки S. При этом подсчитываются только непересекающиеся вхождения. При указании трех параметров S.count(T, a, b), будет выполнен подсчет числа вхождений строки T в срезе S[a:b].
+ ``rjust, ljust`` - позиционирует вправо/слева указанную строку, дополняя её слева до указанной длины указанным символом
+ ``.lower()`` - нижний регистр
+ ``.upper()`` - верхний регистр
+ ``.title()`` - Заглавные буквы
+ ``.split()`` - разделяет строки на кусочки по разделителю
+ ``.join()`` - склеивает строки обратно
+ ``.strip()`` - удаляет пробелы только в начале и в конце строки