University: [ITMO University](https://itmo.ru/ru/)   
Faculty: [FICT](https://fict.itmo.ru)   
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)    
Year: 2024/2025   
Group: K4111c    
Author: Tiurina Alina Dmitrievna    
Lab: Lab4    
Date of create: 07.12.2024    
Date of finished: 21.12.2024        
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
Создаем манифест Deployment и Service. (Рис. 9, 10)     
![Screenshot 9](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/9.jpg)     
Рисунок 9 - Создание манифеста Deployment     
![Screenshot 10](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/10.jpg)     
Рисунок 10 - Создание манифеста Service     
Далее применяем написанные манифесты и производим их проверку. (Рис. 11)     
![Screenshot 11](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/11.jpg)     
Рисунок 11 - Применение написанных манифестов и осуществление их проверки    
Осуществляем подключение к контейнерам, пробросив порты. (Рис. 12)    
![Screenshot 12](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/12.jpg)     
Рисунок 12 - Проброс портов     
Подключаемся к веб-сайту. (Рис. 13)   
![Screenshot 13](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/13.jpg)     
Рисунок 13 - Подключение к веб-сайту   
Отправляем эхо-запросы, используя команду kubectl exec deployment-977pld6b9-6b67p -- ping 10.244.117.110. (Рис. 14)  
![Screenshot 14](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/14.jpg)        
Рисунок 14 - Отправка эхо-запросов     
Схема организации контейнеров и сервисов представлена на рисунке 15.   
![Screenshot 15](https://github.com/Adalin43/2024_2025-introduction_to_distributed_technologies-k4111c-tiurina_a_d/blob/main/lab4/image/15.jpg)        
Рисунок 15 - Схема организации контейнеров и сервисов       

**Результаты лабораторной работы.**          
- Файлы с разработанными манифестами с расширением .yaml.     
- Схема организации контейеров и сервисов, нарисованная в draw.io.    
- Скриншоты c результатами работы.   
