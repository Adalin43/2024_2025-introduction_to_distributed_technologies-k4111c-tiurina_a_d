University: [ITMO University](https://itmo.ru/ru/)   
Faculty: [FICT](https://fict.itmo.ru)   
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)    
Year: 2024/2025   
Group: K4111c    
Author: Tiurina Alina Dmitrievna    
Lab: Lab4    
Date of create: 07.12.2024    
Date of finished:     
**Лабораторная работа №4**    
**Сети связи в Minikube, CNI и CoreDNS.**     
**Описание.**    
В данной работе необходимо познакомиться с сетями связи в Minikube. Особенность Kubernetes заключается в том, что у него одновременно работают underlay и overlay сети, а управление может быть организованно различными CNI.    
**Цель работы.**     
Познакомиться с CNI Calico и функцией IPAM Plugin, изучить особенности работы CNI и CoreDNS.     
**Ход работы.**    
При запуске minikube устанавливаем плагин CNI=calico и режим работы Multi-Node Clusters одновеременно, в рамках данной лабораторной работы необходимо развернуть 2 ноды. (Рис. 1)       
![Screenshot 1](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/1.jpg)     
Рисунок 1 - Установка плагина CNI=calico и режима работы Multi-Node Clusters одновеременно   
Проверяем работу CNI плагина Calico и количество нод. (Рис. 2, 3)   
![Screenshot 2](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/2.jpg)     
Рисунок 2 - Проверка создания нод   
![Screenshot 3](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/3.jpg)    
Рисунок 3 - Проверка работы CNI Calico    
Для проверки режима IPAM для запущеных ранее нод указываем label. (Рис. 4)   
![Screenshot 4](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/4.jpg)    
Рисунок 4 - Проверка режима IPAM        
После этого разрабатываем манифест IPPool. (Рис. 5)   
![Screenshot 5](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/5.jpg)    
Рисунок 5 - Разработка манифеста IPPool    
Применяем написанный манифест. (Рис. 6)   
![Screenshot 6](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/6.jpg)    
Рисунок 6 - Применение написанного манифеста   
Удаляем IPPool по умолчанию. (Рис. 7)   
![Screenshot 7](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/7.jpg)     
Рисунок 7 - Удаление IPPool   
На рисунке 8 видно, что IPPool'ы корректно созданы.   
![Screenshot 8](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/8.jpg)     
Рисунок 8 - Корретное создание IPPool


Создаем deployment с 2 репликами контейнера ifilyaninitmo/itdt-contained-frontend:master и передаем переменные в эти реплики: REACT_APP_USERNAME, REACT_APP_COMPANY_NAME.    
Создаем сервис, через который будет доступ на эти "поды".    
Запускаем в minikube режим проброса портов и подключаемся к контейнерам через веб-браузер.     
Проверяем на странице в веб-браузере переменные Container name и Container IP.      
Используя kubectl exec, заходим в любой "под" и попробуем попинговать "поды", используя FQDN имя соседенего "пода".   

**Результаты лабораторной работы.**       
- Файлы с разработанными манифестами с расширением .yaml.    
- Схема организации контейеров и сервисов, нарисованная в draw.io.   
- Скриншоты c результатами работы.  
