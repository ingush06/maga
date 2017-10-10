# maga
Для авторизации используется все эти параметры обязательно:

HTTP
http://ingfilm.ru/api.php?method=search&login=логин&pass=пароль


Все входные данные принимаются через GET параметры.
Формат выходных данных - JSON.
Пример GET запроса по параметру xf=year|год:
HTTP
http://ingfilm.ru/api.php?method=search&login=zohan&pass=wasd12345&xf=year|2017


Пример ответа API для фильма:
JSON
{
"count": 20,
"items": [
{
"id": "14593",
"title": "Мик",
"date": "2017-10-03 18:32:31",
"category": "7",
"comm_num": "1",
"vote_num": "9",
"news_read": "170",
"tags": "Мик, США",
"year": "2017",
"poster": "http://ingfilm.ru/uploads/posts/2016-12/1483062411-1323152019.jpg",
"country": "США",
"quality": "HD",
"sd": "IdeaFilm",
"id_kinopoisk": "977496",
"description": "Неблагополучная и сквернословящая молодая женщина переезжает в зажиточный Гринвич, Коннектикут, чтобы присматривать за избалованными детьми своей богатой сестры и ее мужа, которые бежали из страны, спасаясь от федерального иска. Она быстро понимает то, что другие давно знают: чужие дети ужасны."
}


Структура JSON объектов:

id - Ид фильма или сериала (не из кинопоиска)
title - Название на русском
date - Дата добавления
category - Номер категории (на пример категория 7 для сериалов)
comm_num - Рейтинг хорошо
vote_num - Рейтинг плохо
news_read - Просмотры
tags - Теги
year - Год
poster - Постер
country - Страна
quality - Качество
sd - Озвучка
id_kinopoisk - Ид кинопоиска
description - Описание


Пример GET запроса по параметру cn для вывода по странам:

HTTP
http://ingfilm.ru/api.php?method=search&login=zohan&pass=wasd12345&xf=cn|Россия


Пример GET запроса по параметру oreder который может принимать два значения ASC и DESC сортировка ASC - по возрастанию. DESC - по убыванию:

HTTP
http://ingfilm.ru/api.php?method=search&login=zohan&pass=wasd12345&xf=cn|Россия&order=DESC
