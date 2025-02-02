Простой контейнер для php + apache webserver. Подготовлен для запуска в кластере Kubernetes.

# Установка
Загрузить файлы Dockerfile, index.php и custom.conf из репозитария.
Запустить в директории с файлыми:

*docker build -t my_appache_php:v1 .*

Загрузить созданный образ в DockerHub:

*docker tag my_appache_php:v1 ваш_логин/ваш_репозитарий_DockerHub:latest* 
*docker push ваш_логин/ваш_репозитарий_DockerHub:latest* 

Для запуска локально в Docker-е выполнить:

*docker run -it -p 1234:80 ваш_логин/ваш_репозитарий_DockerHub:latest*

# Результат при подключении в браузере на порт 1234:
<img src="https://github.com/WSQ-coder/Docker-Kubernetes/Screens/Apache_php/Result.png?raw=true"/>