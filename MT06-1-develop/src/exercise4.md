## Примеры эндпоинтов

Эндпоинт мы будем записывать следующим образом: `{METHOD} /api/{VERSION}/{CLASS}`. 

- METHOD — GET, POST и т.д.
- VERSION — версия API (в нашем случае будем использовать `v1`)
- CLASS — класс объектов, к которому мы обращаемся. Обычно они соответствуют названиям классов в программировании или коллекций в базе данных. К примеру, если там указано значение `users`, то эндпоинт `GET /api/v1/users`, вероятно, отвечает за _получение_ списка пользователей. Давай рассмотрим другой эндпоинт: `POST /api/v1/collection`. Скорее всего, он отвечает за добавление какой-то коллекции. 

В задании же требуется описать 4 эндпоинта с методами из CRUD (один эндпоинт на каждый метод). Тему приложения ты уже знаешь!

## Эндпоинты

1. GET /api/v1/new-year/dishes/recipes - этот запрос позволяет получить список всех новогодних рецептов, которые доступны в системе. 

2. POST /api/v1/new-year/dishes/recipe - этот запрос позволяет создать новый новогодний рецепт в системе. 
```
Response body: 
{
"title": "Новогодний салат из курицы и ананаса",
"ingredients": [
"Яйцо куриное",
"Ананас",
"Сыр полутвердый",
"Орехи кедровые",
"Майонез"
],
"description": "Мелко нарезать курицу на кусочки. 
На тарелку выложить нарезанное куриное филе и смазать его небольшим количеством майонеза. 
Солить мясо не нужно.Очистить варёные и охлаждённые яйца от скорлупы. 
Отделить желтки от белков. Натереть белки на мелкой тёрке. 
Выложить натёртые белки в кольцо поверх курицы, смазать небольшим количеством майонеза.  
Посыпать всю поверхность белков с майонезом ядрами кедрового ореха. 
Выложить нарезанные кусочки ананаса в сервировочное кольцо и разровнять их по всей поверхности желтков. 
Смазать ананас небольшим количеством майонеза. 
Натереть сыр на мелкой тёрке.  
Посыпать всю поверхность салата натёртым сыром и слегка разровнять его. 
Новогодний салат из курицы и ананаса готов. 
Приятного аппетита!"
}
```

3. PUT /api/v1/new-year/dishes/recipe/{2} - этот запрос позволяет обновить информацию о новогоднем рецепте по его идентификатору. 

URL: https://goodfood.com//api/v1/new-year/dishes/recipe/2 
```
Response body: 
{
"title": "Новогодний салат из курицы и ананаса",
"ingredients": [
"Яйцо куриное",
"Рис",
"Филе курицы",
"Маслины",
"Томат",
"Майонез"
],
"description": "Яйца отварите вкрутую за 10 минут, рис и филе — до готовности. 
Куриное мясо, лук, помидоры и маслины нарежьте небольшими кусочками. 
Белки и желтки по отдельности натрите на крупной или средней тёрке. 
Поместите на плоскую тарелку рис так, чтобы получились очертания снегиря, и смажьте майонезом. 
Дальше выложите курицу, лук, желтки и белки. 
После каждого слоя, кроме белкового, смазывайте соусом. 
Из помидоров выложите грудку и клюв снегиря, из маслин — голову, крылья и хвост. 
Из лука сделайте веточки."
}
```

4. DELETE /api/v1/new-year/dishes/recipe/{2} - этот запрос позволяет удалить конкретный новогодний рецепт по его идентификатору. 

URL: https://goodfood.com/api/v1/new-year/dishes/recipe/2
