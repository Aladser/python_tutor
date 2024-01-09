# Функции

Функция ```factorial()```, один параметр — число, и возвращает значение — факториал этого числа.

```
def factorial(n):
    res = 1
    for i in range(1, n + 1):
    res *= i
    return res
```

## Значения по умолчанию

Функция со значениями по умолчанию

```
def check(prices, tip=10):
  sum_ = sum(prices)
  total = sum_ * ( 100 + tip ) / 100
  return total
```

## Именованные аргументы

Функция с именованными аргументами:

```
def get_max(first=0, second=0):
    if first > second:
        return first
    return second

get_max(first=1, second=2)
```
## Любое количество аргументов
Мы можем принимать любое количество аргументов, если при попадании внутрь функции они превращаются в список.

```
def new_sum(*nums):        |
# Запакованные аргументы
  sum = 0
  # nums будет равен [1, 1, 1]
  for n in nums:
    sum += n
  return sum

print(new_sum(1, 1, 1))
```

Мы также можем передать несколько обязательных позиционных аргументов, а затем передать параметры, которые будут запакованы в переменную. Например:

```
def remove_from_string(string, *symbols_to_remove):
  for symbol in symbols_to_remove:
    string = string.replace(symbol,"")
  return string
remove_from_string("О! Смотри, можно удалить все знаки препинания сразу?", "?", "!", ",", ".", "–")
```

