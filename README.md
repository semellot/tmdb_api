# TMDB API #
Проект для работы с API сайта [TMDB](https://www.themoviedb.org/).
С помощью скриптов вы сможете создать БД с информацией о фильмах, и делать поиск по фильмам в этой БД.

Перед началом работы со скриптами необходимо создать API ключ по [инструкции](https://developers.themoviedb.org/3/getting-started/introduction).


## Скрипт hello_api_TMDB.py ##
Проверяет работу API.
После запуска скрипта необходимо ввести ключ API.
Если ключ верный, то выведется число 4000000.

## Скрипт make_own_db.py ##
Создает файл `MyFilmDB.json` с 1000 случайных фильмов из всей библиотеки сайта TMDB.

## Скрипт find_similar.py ##
Поиск похожих фильмов по параметрам: коллекция, язык оригинала, бюджет, жанр.
При запуске скрипта необходимо ввести название файла с базой фильмов.
Затем ввести название фильма для которого нужно найти похожие фильмы.
В результате получим список из похожих фильмов.
Пример запуска скрипта:
```
% python find_similar.py
Enter path to DataBase:MyFilmDB.json
Enter film to search for:Ariel
Four Rooms
Hable con ella
Judgment Night
Kunstgriff
Las Hurdes
Megacities
Sonntag im August
The Dark
Varjoja paratiisissa
```
## Скрипт search_in_db.py ##
Поиск фильмов по названию.
При запуске скрипта необходимо ввести название файла с базой фильмов.
Затем ввести строку поиска.
Пример запуска скрипта:
```
% python search_in_db.py
Enter path to DataBase:MyFilmDB.json
Enter film to search for:dark
Dancer in the Dark
The Dark
```

## Файл own_db_helpers.py ##
Файл содержит вспомогательную функцию `load_data`.
Функция принимает один параметр `path` - путь к БД фильмов.
Возвращает содержимое файла в формате json.

## Файл tmdb_helpers.py ##
Файл содержит вспомогательные функции с запросами к API TMDB.
