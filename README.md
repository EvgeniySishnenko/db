#### Задание 1
Чтобы в будущем вам было легче работать с **MongoDB**, изучите раздел 
документации про использование [**CRUD Operations**](https://docs.mongodb.com/manual/crud/)

#### Задание 2
В файле **README.md** написать следующие запросы для **MongoDB**:
####  - Запрос(ы) для *вставки* данных минимум о двух книгах в коллекцию **books**
 ```sql
db.books.insertMany([
{
  _id:1
  title: "title1",
  description: "description1",
  authors: "authors1"
},{
  _id:2
  title: "title2",
  description: "description2",
  authors: "authors2"
}])
```
 
#### - Запрос для *поиска* полей документов коллекции **books** по полю *title*
 ```sql
 db.books.find({title: "title2"})
```
#### - Запрос для *редактирования* полей: *description* и *authors* коллекции **books** по *_id* записи
 ```sql
 db.books.updateOne({_id: 1},{$set{description: 'update description',{authors: 'update authors ' } }})
```
 
*Каждый документ коллекции **books** должен содержать следующую структуру данных: 
```javascript
{
  title: "string",
  description: "string",
  authors: "string"
}
``` 
