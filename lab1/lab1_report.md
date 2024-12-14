University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)   
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)   
Year: 2024/2025  
Group: K4111c  
Author: Tiurina Alina Dmitrievna  
Lab: Lab1  
Date of create: 07.12.2024  
Date of finished:   

**Лабораторная работа №1.  
Установка Docker и Minikube, мой первый манифест.**  
**Описание.**    
Это первая лабораторная работа, в которой тестируется Docker, устанавливается Minikube и реализуется первый "под".  
**Цель работы.**    
Цель лабораторной работы заключается в ознакомлении с инструментами Minikube и Docker, реализации своего первого "пода".  
**Ход работы.**  
Устанавливаем Docker и Minikube на рабочий компьютер. После установки необходимо развернуть minikube cluster с помощью команды minikube start. (Рис. 1)    
![Screenshot 1](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/1.1.jpg)    
Рисунок 1 - Использование команды minikube start   
Далее скачиваем образ. (Рис. 2)  
![Screenshot 2](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/2.jpg)   
Рисунок 2 - Скачивание образа HashiCorp Vault  
Создаем контейнер на основе образа. (Рис. 3)  
![Screenshot 3](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/3.jpg)   
Рисунок 3 - Создание контейнера на основе образа  
Проверяем, что контейнер был корректно создан. (Рис. 4)  
![Screenshot 4](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/4.jpg)    
Рисунок 4 - Проверка корректного создания контейнера   
Создаем файл laboratory1.yaml для развертывания пода с полученным образом. (Рис. 5)  
![Screenshot 5](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/5.jpg)   
Рисунок 5 - Написание манифеста  
Применяем манифест, используя команду kubectl apply -f laboratory1.yaml. (Рис. 6)  
![Screenshot 6](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/6.jpg)  
Рисунок 6 - Применение манифеста  
Проверяем  появление Pod, используя команду kubectl get pods. (Рис. 7)  
![Screenshot 7](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/7.jpg)     
Рисунок 7 - Проверка Pod   
Добавляем сервис для доступа к созданному контейнеру. (Рис. 8)  
![Screenshot 8](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/8.jpg)   
Рисунок 8 - Создание сервиса для доступа к контейнеру  
Команда minikube kubectl -- port-forward service/vault 8200:8200 позволяет minikube прокинуть порт компьютера в контейнер. Теперь можно зайти в Vault по ссылке http://localhost:8200. С помощью команды minikube kubectl -- logs service/vault находим токен для авторизации. (Рис. 9) 
![Screenshot 9]()  
Рисунок 9 - Поиск токена для авторизации   
Unseal Key: rZCttPCTCaLgYZO/kbTYi2G5h5syNZEoMz0ydcdsQlY=  
Root Token: hvs.IKwqwYCfpsBLOaMOMh9WSlEr  
Далее вводим токен на странице http://localhost:8200. (Рис.10)   
![Screenshot 10]()   
Рисунок 10 - Страница авторизации  
Произведена успешная авторизация. (Рис. 11)  
Рисунок 11 - Успешная авторизация  
Останавливаем Minikube с помощью команды minikube stop.  
Схема организации контейнеров и сервисов представлена на рисунке 12.  
![Screenshot 10]()    
Рисунок 12 - Схема организации сервисов и контейнеров  






