# Фильмы с TMDB

Скрипты для поиска фильмов в базе TMDB.</br>

Для начала нужно установить `Python3, pip3`.</br>
После, установить зависимости с файла `requirements.txt`.
Все скрипты, кроме вспомогательных таких как: `own_db_helpers.py` и `tmdb_helpers.py` можно запускать в директории проекта с терминала.</br>
Например:

```python
python имя_скрипта
```

## Скрипты

### find_similar.py
Пользователю нужно ввести путь к базе данных фильмов и название фильма.
Ecли нет такой базы, пользователь получит сообщение: `File not found, sorry...`.
Если в базе нет такого фильма, система выводит сообщение: `No such film in FilmsDB`.
Когда все данные введены правильно, пользователь получает список рекомендованных фильмов похожие по жанру, по бюджету, по языку и по коллекции.


### hello_api_TMDB.py
Возвращает бюджет фильма по номеру 215. Если api_key правильный. В противном случае, получаем сообщение: `Invalid api key`


### own_db_helpers.py
Пользователь должен ввести api_key. Если ключ не правильный получаем сообщение: `Invalid api key`
Если ключ правильный, выгружаем из базы в файл в формате JSON. Во время выгрузки, консоль показывает процентное соотношение выгрузки.


### search_in_db.py
Пользователь должен ввести путь к базе фильмов. Если путь неправильный, выводится сообщение: `File not found sorry...`
Если путь к базе правильный, пользователью нужно ввести название фильма для поиска в базе. После, на экране появится отсортированный список фильмов.


### tmdb_helpers.py
Вспомогательный файл для работы с `API TMDB`: создание запроса, выгрузка данных в формате `JSON` и проверка `api_key` пользователя
