# SVO

## Краткое описание решения 
Разработана математическая модель, прогнозирующая потребительскую активность в Международном аэропорте Шереметьево. 
[Решение](/SVO%20final%20solution.ipynb), [Предсказанные значения на 06.2022](/svo_submission.csv)

## Источники данных

- Расписание вылетов и прилетов [Расписание](/svo_hack_data/Расписание%20рейсов%2005-06.2022.xlsx)
- Онлайн-табло с сайта Аэрофлота ([Онлайн табло группы Аэрофлот], [Пример запроса онлайн табло])
- Список аэропортов ([Список аэропортов])
- Список самолетов и их компановка ([Самолеты Аэрофлота], [Самолеты России])
- Погода в аэропортах вылета и прилета ([Источник METAR], [Пример запроса METAR])
- Схема аэропорта Шереметьево ([Схема аэропорта Шереметьево])
- Выручка торговых точек ([05.2022](/svo_hack_data/05.2022_Выручка.xlsx), [06.2022](/svo_hack_data/06.2022_Выручка.xlsx))


## Итоги

- Собранны данные из несколько датасетов
- Разработаны модели машинного обучения для прогнозирования выручки торговых точек.
- Определены ключевые признаки, которые влияют на выручку каждой торговой точки


## Инструменты:
python, pandas, numpy, matplotlib, catboost, geopy, requests, swifter, requests, seaborn, metar


## Уникальность 
Разработанное решение позволяет в высокой точностью спрогнозировать выручку в будущем, а также позволяет смоделировать потребительскую активность по более 40 входным параметрам

## Описание файлов 
- [Решение](/SVO%20final%20solution.ipynb)
- [Скрипт скачивания погоды в аэропортах, куда есть прямые рейсы из SVO](/svo_weather.ipynb)
- [Скрипт скачивания информации о вылетах из SVO / прилетах в SVO авиакомпаниями Аэрофлот и Россия за май-июнь 2022 года](/svo_weather.ipynb)
- [Построенные модели](/svo_hack_model)
- [Ключевые признаки для каждой торговой точки](/svo_hack_images)
- [Компановка самолетов Аэрофлота и России](/svo_hack_data/aircraft_seats.csv)
- [Описание параметров, используемых для построения ML модели](/svo_hack_data/Описание%20параметров.xlsx)
- [Погода в аэропортах, куда есть прямые рейсы из SVO](/svo_hack_data/svo_weather.csv)

[Самолеты Аэрофлота]: https://www.aeroflot.ru/ru-ru/about/plane_park
[Самолеты России]: https://www.rossiya-airlines.com/about/about_us/fleet/vozdushnye_suda/
[Источник METAR]: https://mesonet.agron.iastate.edu/request/download.phtml?network=RU__ASOS
[Пример запроса METAR]: https://mesonet.agron.iastate.edu/cgi-bin/request/asos.py?station=UUEE&data=all&year1=2022&month1=4&day1=29&year2=2022&month2=7&day2=2&tz=Etc%2FUTC&format=onlycomma&latlon=no&elev=no&missing=empty&trace=0.0001&direct=no&report_type=3
[Схема аэропорта Шереметьево]: https://www.svo.aero/ru/map?terminal=b&floors=3&zone=all&parentId=338&type=map_menu
[Список аэропортов]: https://www.flightradar24.com/_json/airports.php
[Онлайн табло группы Аэрофлот]: https://flights.aeroflot.ru/ru-ru/onlineboard/arrival/SVO/19112022-0000-2400
[Пример запроса онлайн табло]: https://flights.aeroflot.ru/api/flights/v1.1/ru/board?type=onlineboard&arrival=SVO&dateFrom=2022-05-11T00:00:00&dateTo=2022-05-11T00:00:00&timeFrom=00:00:00&timeTo=23:59:59&returnTo=23:59:59

## Ссылка на соревнование
https://hacks-ai.ru/championships/758467