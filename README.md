[![Django-app workflow](https://github.com/sonoffjord/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg?branch=master)](https://github.com/sonoffjord/yamdb_final/actions/workflows/yamdb_workflow.yml)
### Технологии
В проекте используются:
- Python 3.8.5
- Django 3.0.5
- Docker

Для запуска проекта на локальном компьютере необходио выполнить следующий ряд действий:
- Открываем терминал в склонированной ранее папке
- Создаем образ Docker командой
```
sudo docker build -t <ИМЯ_ВАШЕГО_АККАУНТА>/<ИМЯ_ВАШЕГО_ОБРАЗА_НА_DOCKERHUB>:<ВЕРСИЯ_ВАШЕГО_ОБРАЗА> .
```
- После создания образа загружаем его на DockerHub
```
sudo docker push <ИМЯ_ВАШЕГО_АККАУНТА>/<ИМЯ_ВАШЕГО_ОБРАЗА_НА_DOCKERHUB>:<ВЕРСИЯ_ВАШЕГО_ОБРАЗА>
```
- Заходим на сервер через SSH и устанавлеваем туда Docker
```
sudo apt install docker.io
```
- Если на сервере установлен nginx его необходимо остановить командой
```
sudo systemctl stop nginx
```
- Создаем секреты для репозитория
- Делаем push с локального компьютера
- Открываем браузер, вводим в адресную строку <ip_address_вашего_сервера>/api/v1/. Чтобы посмотреть на запущенный сервер перейдите по адресу 84.201.168.63/api/v1/
