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
Устанавливаем Docker и Minikube на рабочий компьютер. После установки необходимо развернуть minikube cluster с помощью команды minikube start (Рис. 1).    
![Screenshot 1](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/1.1.jpg)    
Рисунок 1 - Использование команды minikube start   
Далее скачиваем образ (Рис. 2).  
![Screenshot 2](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/2.jpg)   
Рисунок 2 - Скачивание образа HashiCorp Vault  
Создаем контейнер на основе образа (Рис. 3).  
![Screenshot 3](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/3.jpg)   
Рисунок 3 - Создание контейнера на основе образа  
Проверяем, что контейнер был корректно создан (Рис. 4).  
![Screenshot 4](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab1/imagine/4.jpg)    
Рисунок 4 - Проверка корректного создания контейнера  


Далее в соотвествии с инструкцией устаналиваем Minikube. После установки необходимо развернуть minikube cluster. Скачиваем Vault, вводим команду ".\vault.exe" (Рис. 2).
![Screenshot 2](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/1.3.jpg)  
Рисунок 2 - Выполнение команды .\vault.exe   
Добавляем путь C:\Users\Dns\Desktop\vault_1 в переменную среды PATH (Рис. 3).  
![Screenshot 3](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/1.5.jpg)  
Рисунок 3 - Добавление пути в переменную среды PATH  
Используем команду minikube start, далее после запуска minikube cluster используем команду minikube kubectl, которая позволяет взаимодействовать с k8s (Рис. 4).  
![Screenshot 4](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/1.4.jpg)  
Рисунок 4 - Использование команд minikube start и minikube kubectl соответственно  
Далее используем команду ".\vault.exe server -dev". Результаты представлены на рисунках 5, 6.  
![Screenshot 5](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/1.6.jpg)   
Рисунок 5 - Результат команды .\vault.exe server -dev  
![Screenshot 6](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/1.7.jpg)   
Рисунок 6 - Результат команды .\vault.exe server -dev (продолжение)  

Unseal Key: s3LHmncxjkZs4kik4BXzyIhmYaiExcA0ccPHCAVfV6I=  
Root Token: hvs.z30D3WdviqIyp4qowYVZ8TjN  

В PowerShell используем команды "$env:VAULT_ADDR="http://127.0.0.1:8200" и ".\vault.exe status" (Рис. 7).   
![Screenshot 7](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/1.9.jpg)   
Рисунок 7 - Использование команд $env:VAULT_ADDR="http://127.0.0.1:8200 и .\vault.exe status  
В браузере вводим "http://localhost:8200" и вводим сгенерированный ранее Token (Рис. 8).  
![Screenshot 8](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/1.10.jpg)   
Рисунок 8 - Ввод сгенерированного Token   
Из рисунка 9 видно, что вход успешно осуществлен.  
![Screenshot 9](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/1.11.jpg)  
Риунок 9 - Успешный вход  
