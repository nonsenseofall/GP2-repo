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

- 0   source         12014 non-null  object 
- 1   name           12013 non-null  object 
- 2   genres         11987 non-null  object 
- 3   released       12014 non-null  object 
- 4   metacritic     3907 non-null   float64
- 5   rating         12014 non-null  float64
- 6   platforms      12008 non-null  object 
- 7   developers     11781 non-null  object 
- 8   publishers     11526 non-null  object 
- 9   playtime       11288 non-null  float64
- 10  reviews_count  11288 non-null  float64
  
## metacritics_edited ##

-  0   Unnamed: 0         13949 non-null  int64  
-  1   page               13949 non-null  int64  
-  2   title              12147 non-null  object 
-  3   url                13949 non-null  object 
-  4   name_parsed        13949 non-null  object 
-  5   rating             11647 non-null  object 
-  6   company            0 non-null      float64
-  7   release_date       13920 non-null  object 
-  8   platforms          13949 non-null  object 
-  9   genres             13949 non-null  object 
-  10  summary            13908 non-null  object 
-  11  metascore          13925 non-null  object 
-  12  metascore_amount   13924 non-null  object 
-  13  user_score         13925 non-null  object 
-  14  user_score_amount  12424 non-null  object

## merged_clean(last_version) ##

-  0   title              13960 non-null  object 
-  1   rating_parsed      11656 non-null  object 
-  2   release_date       13931 non-null  object 
-  3   platforms_parsed   13960 non-null  object 
-  4   genres_parsed      13960 non-null  object 
-  5   metascore          13924 non-null  float64
-  6   metascore_amount   13960 non-null  int64  
-  7   user_score         12428 non-null  float64
-  8   user_score_amount  13960 non-null  int64  
-  9   developers         6023 non-null   object 
-  10  publishers         4188 non-null   object 
