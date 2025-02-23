
# Лабораторная работа 4.

## Процесс выполнения
### Создание и настройка контейнеров
Для выполнения лабараторной работы буду использовать Docker для Windows с WSL.
Создаем две папки для наших контейнеров:
- /d/Repositories/lab4/container-1
- /d/Repositories/lab4/container-2

Теперь создаем наш докерфайл:
```bash
touch Dockerfile
```
и прописываем в него такое содержимое:
![image](assets/1.png)

Копируем:
```bash
cp Dockerfile ../container-2
```
Проверяем работу контейнеров:
```bash
docker build -t container-1 .
dcoker run -it --name con1 container-1
```
![image](assets/2.png)
(Git Bash здесь меня подвел, использую CMD.EXE)
__Аналогично со вторым контейнером.__

### Создание и проверка работы сети
Создаем нашу сеть и присоединяем контейнеры:
```bah
docker network create myNet
docker network connect myNet con1
docker network connect myNet con2
```
![image](assets/3.png)
