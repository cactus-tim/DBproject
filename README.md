# DBproject
TODO:
Прописать в логической модели и физической модели нормальные названия имен таблиц большими буквами 

1. Состав команды: Ефимов Александр, Ильин Павел, Кулешов Илья, Прошин Антон, Соснин Тимофей

Область: стратегическая игра для мобильных устройств
Список сущностей: 
Факты: 
PLAYERS_X_BUILDS
PLAYERS_X_RESURSES 
PLAYERS_X_WARRIORS

Измерения: 
PLAYERS
BUILDS
RESURSES
WARRIORS
INTERSHIPS
INTERSHIPS_RES
INTERSHIPS_TYPE

2. БД находится в 2НФ, где каждый атрибут в таблице должен быть функционально зависим только от первичного ключа. Каждая запись в таблице имеет уникальный идентификатор, который позволяет однозначно идентифицировать каждую запись.

Таблицы WARRIORS и BUILDS - версионные, выбрали SCD2, те вместо замены старых данных новыми, каждое изменение создаёт новую запись, сохраняя при этом старые версии.

Поэтому добавим "WARRIORS_HISTORY", триггер будет создавать запись в таблице "WARRIORS_HISTORY" каждый раз, когда в таблице "WARRIORS" происходит обновление. В таблице "WARRIORS_HISTORY" будут храниться старые значения полей войнов.

Добавим "BUILDS_HISTORY", триггер будет создавать запись в таблице "BUILDS_HISTORY" каждый раз, когда в таблице "BUILDS" происходит обновление. В таблице "BUILDS_HISTORY" будут храниться старые значения полей зданий.
