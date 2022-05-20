# Сборка библиотеки banking в контейнере docker (с использованием файлов,хранящихся в репозитории github)
## 1. Создаём образ контейнера на основе Dockerfile
> docker build -t <имя_контейнера> .

## 2. Создаём контейнер образа 
> docker run -it <имя_образа> 

## 3. Клонируем репозиторий с github.
> git clone https://github.com/AstorBrom/lab-05

## 4.Собираем библиотеку
> cd lab-05
> cmake -H. -B build
> cd build
> make
> exit
