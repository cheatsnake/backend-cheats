# Шпаргалка по MongoDB

<div align="right"><a href="https://github.com/cheatsnake/backend-cheats#mongodb">Вернуться на главную страницу ⬆️</a></div>

-   Подготовка БД

```js
show dbs // показать список всех БД
use db_name // подключиться/создать БД с именем db_name
db // вывести имя текущей базы данных
db.createCollection("users") // создать коллекцию "notes"
show collections // показать список коллекций в текущей БД
db.dropDatabase() // удалить текущую БД
```

-   Добавление элементов

```js
// Добавить один элемент
db.users.insertOne({
    name: "Alex",
    age: 27,
    isMarried: false,
    city: "NewYork"
})

// Добавить несколько элементов
db.users.insertMany([{...}, {...}])
```

-   Получение элементов

```js
// Получить все элементы из коллекции
db.users.find();
// Получить элементы по указанному критерию
db.user.find({ age: 27 });
// Получить один элемент
db.users.findOne({ name: "Alex" });
// Получить отсортированный список элементов
// 1 - по возрастанию; -1 - по убыванию
db.users.find().sort({ age: 1 });
// Получить количество элементов
db.users.find().count();
// Лимит количества получаемых элементов
db.users.find().limit(10);
// Выборка с помощью операторов сравнения
db.users.find({ age: { $gt: 20 } }); // > 20
db.users.find({ age: { $gte: 20 } }); // >= 20
db.users.find({ age: { $lt: 50 } }); // < 50
db.users.find({ age: { $lte: 50 } }); // <= 50
db.users.find({ age: { $ne: 35 } }); // != 35
```

-   Изменение элементов

```js
// Полное изменение элемента (первый аргумент - критерий поиска)
db.users.updateOne({name: "Alex"}, {новые_данные})
// Изменение определенных полей элемента
db.users.updateOne({name: "Alex"}, {$set: {age: 28, isMarried: true}})
// Переименовать поле у нескольких элементов
db.users.updateMany({name: "Alex"}, {&rename: {city: "town"}})
// Удаление элемента/элементов
db.users.deleteOne({name: "Alex"})
db.users.deleteMany({name: "Alex"})
```
