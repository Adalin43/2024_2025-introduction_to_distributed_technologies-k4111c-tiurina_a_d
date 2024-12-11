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
Описание.   
Это первая лабораторная работа, в которой тестируется Docker, устанавливается Minikube и реализуется первый "под".  
Цель работы.   
Цель лабораторной работы заключается в ознакомлении с инструментами Minikube и Docker, реализации своего первого "пода".  
**Ход работы.**  
Устанавдиваем Docker версии 19.03.1 на рабочий компьютер (Рис. 1).  
![Screenshot 1](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/ЛР-1.1.png)  
                              Рисунок 1 - Docker версии 19.03.1  
Далее в соотвествии с инструкцией устаналиваем Minikube. После установки необходимо развернуть minikube cluster. Используем команду minikube start.            
После запуска minikube cluster используем команду minikube kubectl, которая позволяет взаимодействовать с k8s используя команду (Рис. 2).  
