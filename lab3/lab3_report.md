University: [ITMO University](https://itmo.ru/ru/)   
Faculty: [FICT](https://fict.itmo.ru)   
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)   
Year: 2024/2025    
Group: K4111c    
Author: Tiurina Alina Dmitrievna    
Lab: Lab3   
Date of create: 07.12.2024    
Date of finished:    
**Лабораторная работа №3.**    
**Сертификаты и "секреты" в Minikube, безопасное хранение данных.**   
**Описание.**    
В данной лабораторной работе необходимо познакомитесь с сертификатами и "секретами" в Minikube, правилами безопасного хранения данных в Minikube.    
**Цель работы.**  
Познакомиться с сертификатами и "секретами" в Minikube, правилами безопасного хранения данных в Minikube.   
**Ход работы.**   
Создаем configMap с переменными: REACT_APP_USERNAME, REACT_APP_COMPANY_NAME. Манифест для создания configMap записан в файле с расширением .yaml. (Рис. 1)  
![Screenshot 1]()   
Рисунок 1 - Создание манифеста для configMap   

  

Создаем replicaSet с 2 репликами контейнера ifilyaninitmo/itdt-contained-frontend:master и, используя ранее созданный configMap, передаем переменные REACT_APP_USERNAME, REACT_APP_COMPANY_NAME.    

Включаем minikube addons enable ingress и генерируем TLS-сертификат, импортируем сертификат в minikube.    

Создаем ingress в minikube, где указан ранее импортированный сертификат, FQDN, по которому будем заходить, и имя сервиса, который был создан ранее.    

**Если вы делаете эту работу на Windows/macOS для доступа к ingress вам необходимо использовать команду minikube tunnel к созданному ingress. Если вы делаете эту работу на Windows/macOS для доступа к ingress вам необходимо в hosts добавить ip address localhost и ваш FQDN. Если установлен Linux, то нужно указывать minikube ip.**     

В hosts прописываем FQDN и IP адрес ingress и пробуем перейти в браузере по FQDN имени.     

Входим в веб-приложение по FQDN, используя HTTPS, и проверяем наличие сертификата.     

**Обычно в браузере это маленький замочек рядом с FQDN сайта, нажмите на него и сделайте скриншот с информацией.**    


**Результаты лабораторной работы.**     
- Файлы с разработанными манифестами с расширением .yaml.  
- Схема организации контейеров и сервисов, нарисованная в draw.io.  
- Скриншоты c результатами работы.   

