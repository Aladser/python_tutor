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

