# Словари

Структура данных, позволяющая идентифицировать ее элементы по произвольному индексу.

## Создание словаря

`Capitals = dict()`

`Capitals = {'Russia': 'Moscow', 'Ukraine': 'Kiev', 'USA': 'Washington'}`

`Capitals = dict(Russia = 'Moscow', Ukraine = 'Kiev', USA = 'Washington')`

`Capitals = dict([("Russia", "Moscow"), ("Ukraine", "Kiev"), ("USA", "Washington")])`

`Capitals = dict(zip(["Russia", "Ukraine", "USA"], ["Moscow", "Kiev", "Washington"]))`

## Работа с элементами словаря

Основная операция: получение значения элемента по ключу, записывается так же, как и для списков: `A[key]`. Если элемента с заданным ключом нет в словаре, то возникает исключение KeyError.

Другой способ определения значения по ключу — `A.get(key)`. Если элемента с ключом get нет в словаре, то возвращается значение None. В форме записи с двумя аргументами A.get(key, val) метод возвращает значение val, если элемент с ключом key отсутствует в словаре.

Проверить принадлежность элемента словарю можно операциями `in` и `not in`.

Для добавления нового элемента в словарь нужно просто присвоить ему какое-то значение: `A[key] = value`.

Для удаления элемента из словаря можно использовать операцию `del A[key]` (операция возбуждает исключение KeyError, если такого ключа в словаре нет. 

Два безопасных способа удаления элемента из словаря.

`A.pop(key)` - возвращает значение удаляемого элемента. Если элемент с данным ключом отсутствует в словаре, то возбуждается исключение. Если методу pop передать второй параметр, то если элемент в словаре отсутствует, то метод pop возвратит значение этого параметра. Это позволяет проще всего организовать безопасное удаление элемента из словаря: A.pop(key, None).

## Перебор элементов словаря

`A = dict(zip('abcdef', list(range(6))))`

`for key in A:`

&emsp;`print(key, A[key])`

