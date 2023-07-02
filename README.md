# 12.3_K8S_StartApp_Aleksandr_Molokov

### Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod

1. Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
2. После запуска увеличить количество реплик работающего приложения до 2.
3. Продемонстрировать количество подов до и после масштабирования.
4. Создать Service, который обеспечит доступ до реплик приложений из п.1.
5. Создать отдельный Pod с приложением multitool и убедиться с помощью `curl`, что из пода есть доступ до приложений из п.1.

## Ответ

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



