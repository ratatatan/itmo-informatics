## Лабораторная работа 1


1. Создаем наш файл `script.bash`

```bash
touch script.bash
```

2. Открываем в `gedit` и пишем в наш файл:

```bash
#!/bin/bash

echo "Hello, $1!"
```

3. При запуске нашей программы мы получим необходимый результат:

```bash
bash script.bash Timur
```
```bash
Hello, Timur!
```
