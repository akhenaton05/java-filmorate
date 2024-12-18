# ER cхема базы данных Filmorate
Данные для проекта Filmorate представлены в виде реляционной базы данных.
На схеме продемонстрированы отношения между таблицами User и Film.

![ER-diagram](er-diagram.png)

## Описание схемы
В таблице films хранятся данные о фильме(Название, описание, дата выхода, продолжительность, кол-во ценок и рейтинг)

- В таблице films_genres хранятся ключи таблиц films и genres.

- Таблица rating хранит ID и название рейтинга фильма со связью * к 1

В таблице users хранятся данные о пользователе(ID, email, login, дата рождения, имя)

- Таблица users_friends показывает список друзей пользователя, включая их статус

- Таблица users_likes показывает фильмы, которые пользователь добавил в список понравившихся

## Примеры запросов

1. Получение информации о всех фильмах

`SELECT *`

`FROM films;`

2. Получение информации о всех пользователях

`SELECT * `

`FROM users;`

3. Получение топа лучших фильмов

`SELECT *`

`FROM films`

`ORDER BY likes_count DESC`

`LIMIT 5;`

4. Получение название фильма и его рейтинга

`SELECT f.name, r.name`

`FROM films AS f`

`JOIN rating AS r ON f.rating_id = r.rating_id;`


### [Ссылка на ER - диаграмму](https://dbdiagram.io/d/671e8a8197a66db9a36d5e78)





