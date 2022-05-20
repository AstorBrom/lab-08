# Сборка библиотеки banking в контейнере docker (локальные файлов).
## 1. Создаём образ нна основе Dockerfile 
> docker build -t <имя_образа> .

## 2. Создаём контейнер с этим образом
> docker run -it <имя_образа>

## 3. Собираем библиотеку
> cmake -H. -B build 
> cd build
> make
> exit 
