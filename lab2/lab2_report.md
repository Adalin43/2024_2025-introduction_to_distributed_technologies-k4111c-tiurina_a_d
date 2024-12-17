University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)  
Year: 2024/2025  
Group: K4111c  
Author: Tiurina Alina Dmitrievna  
Lab: Lab2  
Date of create: 07.12.2024  
Date of finished:   
**Лабораторная работа №2.**    
**Развертывание веб сервиса в Minikube, доступ к веб интерфейсу сервиса. Мониторинг сервиса.**   
**Описание.**  
В данной лабораторной работе необходимо выполнить развертывание полноценного веб сервиса с несколькими репликами.   
**Цель работы.**  
Ознакомиться с типами "контроллеров" развертывания контейнеров, ознакомиться с сетевыми сервисами и развернуть свое веб приложение.   
**Ход работы.**  
Скачиваем образ ifilyaninitmo/itdt-contained-frontend:master с помощью команды docker pull ifilyaninitmo/itdt-contained-frontend:master. (Рис. 1)  
![Screenshot 1](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/1.jpg)   
Рисунок 1 - Скачивание образа  
Проверяем, что образ корректно установлен. (Рис. 2)  
![Screenshot 2](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/2.jpg)   
Рисунок 2 - Проверка установки образа   
Далее создаем контейнер на основе скаченного образа. (Рис. 3)  
![Screenshot 3](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/3.jpg)   
Рисунок 3 - Создание образа на основе скаченного образа  
Проверяем, что контейнер на основе скаченного ранее образа установлен с помощью команды docker ps -a. (Рис. 4)  
![Screenshot 4](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/4.jpg)   
Рисунок 4 - Проверка созданного контейнера на основе скаченного ранее образа   
Далее запускаем Minikube, используя команду minikube start. (Рис. 5)  
![Screenshot 5](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/5.jpg)   
Рисунок 5 - Запуск Minikube  
Далее создаем deployment с 2 репликами контейнера ifilyaninitmo/itdt-contained-frontend:master и передаем переменные в эти реплики: REACT_APP_USERNAME, REACT_APP_COMPANY_NAME. (Рис. 6)     
![Screenshot 6](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/6.jpg)   
Рисунок 6 - Создание файла laboratory2.yaml   
Применяем созданный манифест для создания реплик. (Рис. 7)   
![Screenshot 7](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/7.jpg)   
Рисунок 7 - Применение написанного манифеста    
Проверяем добавление deployment. (Рис. 8)   
![Screenshot 8](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/8.jpg)    
Рисунок 8 - Проверка добавления deployment   
Создаем сервис, через который будет доступ на эти "поды". (Рис. 9)  
![Screenshot 9](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/9.jpg)    
Рисунок 9 - Создание сервиса  
Применяем его с помощью команды minikube kubectl -- apply -f service.yaml service/frontend-service created. Далее пробрасываем порты для доступа к контейнерам через веб-браузер. (Рис. 10)  
![Screenshot 10](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab2/imagine/10.jpg)   
Рисунок 10 - Проброс портов  
Подключаемся к контейнерам через веб-браузер. (Рис. 11)   
![Screenshot 11]()  
Рисунок 11 - Подключение к контейнерам через веб-браузер   
Запускаем в minikube режим проброса портов и подключаемся к нашим контейнерам через веб браузер.   

Проверяем на странице в веб браузере переменные REACT_APP_USERNAME, REACT_APP_COMPANY_NAME и Container name. ((((Изменяются ли они? Если да то почему?))))    

Проверяем логи контейнеров.   

**Результаты лабораторной работы.**   
- Файлы с разработанными манифестами с расширением .yaml.  
- Схема организации контейеров и сервисов, нарисованная в draw.io.  
- Скриншоты c результатами работы.  
