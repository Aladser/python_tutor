# Файлы

### Открываем файл
```
f = open('text.txt',"r") # на чтение
f = open('text.txt',"w") # на запись
f = open('text.txt',"a") # дозапись в запись
```

### Получаем всё содержимое файла
```
f = open('text.txt')
content = f.read()
print(content)
f.close()
```

### Чтобы кириллица выглядела читаемой под Windows, уточняем кодировку:
```
f = open("text.txt", "r", encoding="utf-8")
```

### Читаем файл построчно 
```
f = open('text.txt')
for line in f:
  print(line)
f.close()
```

### Пишем в файл (заменить содержимое файла)
```
with open('newfile.txt', 'w', encoding="utf-8") as f:
name = input('Ваш пароль' )
f.write(name + '\n')
```

### Как дописать данные в файл
```
with open('text.txt', 'a') as f:
print(f.write("Эта строчка идет в конец файла"))
```