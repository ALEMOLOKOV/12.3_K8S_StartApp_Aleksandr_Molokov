# 12.3_K8S_StartApp_Aleksandr_Molokov

### Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod

1. Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
2. После запуска увеличить количество реплик работающего приложения до 2.
3. Продемонстрировать количество подов до и после масштабирования.
4. Создать Service, который обеспечит доступ до реплик приложений из п.1.
5. Создать отдельный Pod с приложением multitool и убедиться с помощью `curl`, что из пода есть доступ до приложений из п.1.

## Ответ

Мой файл Deployment - ![)

### Увеличение реплик до 2-х

Для увличения реплик необходимо указать в параметре replicas необходимое количество

### Поды до и после маштабирования

#### 1 реплика

![1 1 1 replica](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/a9247007-66ab-470b-86bd-a83d7d609f39)

#### 2 реплики

![1 1 2 replicas](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/40c05d70-24d5-4f85-9327-50b8645c8488)

### Поды

![1 1 5 создание пода мультитул](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/d7d2a831-cb48-45b1-942d-92bab2645a95)

#### Сервис

![1 1 4 service](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/c28d2859-178a-486a-8fc6-e4aa43c3a998)

#### Доступ 

![ответ 1,1,5](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/4b1f4978-f762-4f0f-ae0e-ffbdf4b8a84b)


------

### Задание 2. Создать Deployment и обеспечить старт основного контейнера при выполнении условий

1. Создать Deployment приложения nginx и обеспечить старт контейнера только после того, как будет запущен сервис этого приложения.
2. Убедиться, что nginx не стартует. В качестве Init-контейнера взять busybox.
3. Создать и запустить Service. Убедиться, что Init запустился.
4. Продемонстрировать состояние пода до и после запуска сервиса.

## Ответ

Ссылка на Deployment - ![Deployment](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/blob/49ce87a166f74a44d69e66c81aa838254ab21501/Deployment.yaml)

Ссылка на Service - ![Service](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/blob/cd0d7d873780023cbf0d1cf20cd323f66030e13b/Service.yaml)

Статус Deployment

![2 1Статус Deployment](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/905b8856-c057-4533-be9f-7b9fd15ee283)

Статус Pods

![2 2Статус Pods](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/85829aea-6b3f-49df-bee4-a8aa5c0928da)

Запуск и проверка Service

![2 3 Запуск и проверка Service](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/68ddc692-bbf8-4325-b6b4-b077aae05c06)

Статус Pods после старта Service

![2 4 Статус подов и проверка nginx после старта сервиса](https://github.com/ALEMOLOKOV/12.3_K8S_StartApp_Aleksandr_Molokov/assets/109212419/6c0349fb-e867-4d65-8f40-1db1618f70b8)



