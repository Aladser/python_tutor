# Правила хорошего тона (PEP 8)

+ После объявления функций ставится два переноса строки:
+ Аргументы разделяются запятой с пробелом:
+ Если есть значения по умолчанию, знаки равно в них НЕ окружаются пробелами:
```
def precheck(prices, tip=10):
```
+ Если имя аргумента конфликтует с зарезервированным словом, мы никак не можем или не хотим придумать другое имя, ставим в конце андер (нижнее подчеркивание):
+ Документировать функции полезно, это можно сделать с помощью """. Такие строки называются docstring или «докстринги»:

```
def remove_from_string(string, *symbols_to_remove):
  """Удаляет символы, перечисленные после первого аргумента  """

  for symbol in symbols_to_remove:
    string = string.replace(symbol,"")
  return string

print(remove_from_string.__doc__)
```