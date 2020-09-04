# Тестовое задание StudyWorld

Есть микро-сервис который умеет принимать запросы через `http` и отдает результат запроса через `websocket`.
Проблема в том что неизвестно сколько времени займет обработка запроса по `http`. Поэтому необходимо реализовать хелпер,
который поможет простым способом получать ответы на запросы. Например: 

```js
request('/payment').then(data => {
    console.log(data);
});
```

## API

### http

- POST `/payment` –– запрос на создание платежа с рандомной задержкой
- POST `/payment?delay=5000` –– запрос на создание платежа с определенной задержкой (в ms)

### WebSocket

- Событие `paymentCreated` -- платеж создан

## Быстрый старт

1. Запускается контейнер

```
docker-compose up --build
```

2. Можно заходить на http://localhost:3000

3. Редактировать код в `./server/index.html`

## Служба моральной поддержки

Скорее всего мы неидеально написали тестовое задание, и вы поможете нам его уточнить, если зададите вопросы. 
Видите какую-то непреодолимую сложность — не играйте в телепатов и экстрасенсов, задайте вопрос.