# Анализ рынка игровой индустрии

## 1. Описание проекта
Наш бизнес-заказчик крупный разработчик игр просит нас провести анализ рынка игровой индустрии для определения некоторых бизнес-инсайтов, проверки гипотез и выыодов о том как выпустить наиболее удачную игру.

## 2. Архитектура решения
- Источник №1 — API ([rawg](https://rawg.io))
- Источник №2 — Scraping ([metacritic](https://www.metacritic.com))
- Объединение данных(merge таблиц)
- Проведение анализа продуктовых гипотез
- Выводы для каждой гипотезы

## 3. Описание данных
### rawg_games_after_cleaning_developers_publisher_playtime_reviews_count ###

- 0   source         12014 non-null  object (ИСТОЧНИК ДАННЫХ)
- 1   name           12013 non-null  object (ИМЯ ПРОЕКТА)
- 2   genres         11987 non-null  object (ЖАНР ИГРЫ)
- 3   released       12014 non-null  object (ДАТА РЕЛИЗА)
- 4   metacritic     3907 non-null   float64 (ОЦЕНКИ НА ДРУГОМ СЕРВИСЕ)
- 5   rating         12014 non-null  float64 (РЕЙТИНГ ИГРЫ (ОЦЕНКА))
- 6   platforms      12008 non-null  object (ПЛАТФОРМЫ У ИГР)
- 7   developers     11781 non-null  object (РАЗРАБОТЧИК)
- 8   publishers     11526 non-null  object (КТО ВЫПУСТИЛ ИГРУ)
- 9   playtime       11288 non-null  float64 (ВРЕМЯ СЮЖЕТНОЙ ЛИНИИ В ИГРЕ)
- 10  reviews_count  11288 non-null  float64 (СЧЕТЧИК ОТЗЫВОВ)
  
## metacritics_edited ##

-  0   Unnamed: 0         13949 non-null  int64  (ИНДЕКСЫ)
-  1   page               13949 non-null  int64  (СТРАНИЦА С КОТОРОЙ ПАРСИЛИ)
-  2   title              12147 non-null  object (ИМЯ ПРОЕКТА)
-  3   url                13949 non-null  object (ССЫЛКА НА ПРОЕКТ)
-  4   name_parsed        13949 non-null  object (ИМЯ ПРОЕКТА)
-  5   rating             11647 non-null  object (РЕЙТИНГ ИГРЫ (ОЦЕНКА))
-  6   company            0 non-null      float64 (РАЗРАБОТЧИК)
-  7   release_date       13920 non-null  object (ДАТА РЕЛИЗА)
-  8   platforms          13949 non-null  object (ПЛАТФОРМЫ У ИГР)
-  9   genres             13949 non-null  object (ЖАНР ИГРЫ)
-  10  summary            13908 non-null  object (ОПИСАНИЕ ИГРЫ)
-  11  metascore          13925 non-null  object (РЕЙТИНГ ИГРЫ (ОЦЕНКА))
-  12  metascore_amount   13924 non-null  object (СЧЕТЧИК ОТЗЫВОВ)
-  13  user_score         13925 non-null  object (РЕЙТИНГ ИГРЫ (ОЦЕНКА))
-  14  user_score_amount  12424 non-null  object (СЧЕТЧИК ОТЗЫВОВ)

## merged_clean(last_version) ##

-   0   title              13960 non-null  object (ИМЯ ПРОЕКТА)
-  1   rating_parsed      11656 non-null  object (РЕЙТИНГ)
-  2   release_date       13931 non-null  object (ДАТА РЕЛИЗА)
-  3   platforms_parsed   13960 non-null  object (ПЛАТФОРМЫ У ИГР)
-  4   genres_parsed      13960 non-null  object (ЖАНР ИГРЫ)
-  5   metascore          13924 non-null  float64 (РЕЙТИНГ ИГРЫ (ОЦЕНКА))
-  6   metascore_amount   13960 non-null  int64 (СЧЕТЧИК ОТЗЫВОВ)
-  7   user_score         12428 non-null  float64 (РЕЙТИНГ ИГРЫ (ОЦЕНКА))
-  8   user_score_amount  13960 non-null  int64  (СЧЕТЧИК ОТЗЫВОВ)
-  9   genres_api         6085 non-null   object (ЖАНР ИГРЫ)
-  10  platforms_api      6092 non-null   object (ПЛАТФОРМЫ У ИГР)
-  11  developers         6023 non-null   object (РАЗРАБОТЧИК)
-  12  publishers         4188 non-null   object (КТО ВЫПУСТИЛ ИГРУ)
