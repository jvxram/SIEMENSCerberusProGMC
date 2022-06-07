Охранно-пожарная сигнализация и сопряжение со смежными системами (общеобменная и противодымная приточно-вытяжная вентиляция, лифты, эскалаторы, газовое пожаротушение в серверных, водяное пожаротушение, свето-звуковая сигнализация, голосовое оповещение)

Место расположения объекта
https://www.google.com/maps/place/The+Main+Media+Centre/@43.4143699,39.9490864,822m/data=!3m1!1e3!4m5!3m4!1s0x40f595659235f989:0x1ce8e70f3fc77050!8m2!3d43.415192!4d39.9504643

Проектная документация на сервере в папке `P:\Сириус Главный Медиа Центр (гп1)\Проектная документация`.

Фото, видеозаписи и исполнительные чертежи в AutoCAD-е разложены на сервере по папкам:
 - `P:\Сириус Главный Медиа Центр (гп1)\Исполнительная документация\Планы и разрезы\Этаж 1`
 - `P:\Сириус Главный Медиа Центр (гп1)\Исполнительная документация\Планы и разрезы\Этаж 2`
 - `P:\Сириус Главный Медиа Центр (гп1)\Исполнительная документация\Планы и разрезы\Этаж 3`
 - `P:\Сириус Главный Медиа Центр (гп1)\Исполнительная документация\Планы и разрезы\Кровля`

![Насосная и компрессорные](https://user-images.githubusercontent.com/104857185/171544261-4c532d6e-1d3c-4a05-ba8e-2b2aca1acf58.JPG)
![7205-V2_Plan - копия](https://user-images.githubusercontent.com/104857185/171543881-4e543708-fdce-4141-bce4-7e9f0f161609.jpg)
![7205 5 4-V2_Plan](https://user-images.githubusercontent.com/104857185/171544022-b674540c-0bbd-43bc-bcbf-c25a29116c45.jpg)
![Компрессорные](https://user-images.githubusercontent.com/104857185/171544346-5e44b47b-49b2-4dbb-85ba-10ddfd316b3c.JPG)

###### Диспетчерская (пом. 2200), Панель 16 (шлюз, GAP)

![IMG_2726](https://user-images.githubusercontent.com/104857185/171537384-c482f8e8-ee0a-4139-be72-2731192d944e.JPG)
![IMG_4644](https://user-images.githubusercontent.com/104857185/171537639-966bbdd7-f238-458b-91cf-18e4e560d9d3.JPG)
![IMG_4838](https://user-images.githubusercontent.com/104857185/171537809-222a04d8-c10b-4a70-8f21-f0596526ad6e.JPG)


###### Версия конфигуратора

![Версия конфигуратора v5](https://user-images.githubusercontent.com/104857185/171536166-94498381-1c9f-4b21-b5d8-3bd6a90bf7b4.png)

Панели и ММ-ка ведут обмен по **BACNet**-у. Ветки сети (см. схему сети C-WEB и SafedLink) с панелями то одна, то другая попеременно отваливаются. В связи с этим надо внести следующие изменения:
 - переключить панели с **SafedLink**-а 384 кбит/сек на локальную подсеть (все панели стоят в кроссовых рядом с коммутаторами локальной подсети),
 - кольцо **C-WEB** на 4 панели оставить,
 - обновить прошивки на панелях до **50.21.88**,
 - обновить ММ-ку **4.40** -> **4.81**,
 - заменить сущ. USB-вый сервисный ключ на объектовый, чтобы задействовать функционал в проекте ММ-ки полностью,
 - переделать ММ-ку с **BACNet**-а на **OPC-сервер**,
 - переключить ММ-ку с комплектного **SQLExpress** на внешний **SQL Server** (Standard), чтобы обслуживать 3 базы данных ММ-ки

###### Схема сети C-WEB и SafedLink

![Схема сети C-WEB](https://user-images.githubusercontent.com/104857185/171630002-21a06402-22ff-4404-8288-f750662044a4.JPG)
![Схема сети C-WEB и SafedLink](https://user-images.githubusercontent.com/104857185/171536790-5f6772e3-4cc1-4c89-a544-cff10c3aa81a.jpg)

###### Адреса 2-х сетевых плат на ММ-ке (слева - конфигуратор, справа - ММ-ка (левая - в Интернет через локальную подсеть, правая - панели)

![IMG_20160816_112309](https://user-images.githubusercontent.com/104857185/172000116-46ac80d0-66b7-4bb0-9fba-a1d3011dfd25.jpg)
![Настройка сетевой платы для конфигуратора](https://user-images.githubusercontent.com/104857185/171536396-04cfb9a4-3505-46ba-a031-703e29f62c0b.png)

###### Статические маршуры между панелями и ММ-кой

![Добавление статического маршрута](https://user-images.githubusercontent.com/104857185/171542264-712bcdad-d6c3-49e7-99fc-c9a0c84540d2.png)

###### SCADA-система DMS8000 (предыдущий нерабочий проект в ММ-ке)

![Версия Composer-а](https://user-images.githubusercontent.com/104857185/171541990-c5dfd4db-58a9-4f4c-8426-c8e2f8cee2c7.png)
![Версия DMS8000 с данными о Hotfix-ах](https://user-images.githubusercontent.com/104857185/171542050-9e56e80a-f688-4796-b051-77f86d28af51.png)
![Версия MM8000](https://user-images.githubusercontent.com/104857185/171542084-919d4cbc-3a68-4d4c-befd-4296c89d606e.png)

###### SCADA-система DMS8000 (данный проект в ММ-ке)
###### Настройка BACNet в компосере ММ-ки

![Настройки BACnet в Composer-е](https://user-images.githubusercontent.com/104857185/171542161-afc7b7ef-1e89-421a-bb9b-b8a58fd44b8a.png)

Указания по считыванию топологии, конфигурированию, рисованию проекта в ММ-ке см. в https://github.com/tsv19su254052/SIEMENSCerberusProAirPortPlatov

----
Общие замечания:

На первичное обследование ходили в августе 2015-го года, когда Омега уходила с этого объекта. Из просмотренной части аппаратуры работающей не обнаружили. Работоспособность остальной части установить не удалось, так как для этого требовалось много времени и ограничились беглым внешним осмотром.

![IMG_2724](https://user-images.githubusercontent.com/104857185/172072793-53b99bb7-8b8d-408a-9ab9-15bb48be7482.JPG)
![IMG_2730](https://user-images.githubusercontent.com/104857185/172072820-2a0623da-faa8-4999-8b7d-eeed5738df79.JPG)

К работам приступили в мае 2016-го года. Сразу планировалось подписать договор и осуществлять обслуживание, которое в том состоянии аппаратуры было конечно не возможно. От диспетчеров слышали утверждение работников предыдущей обслуживающей организации, что "... тут все было и все работало ...". Договорились начать восстановительные работы без уточнения объемов и сроков по договору на обслуживание. Восстановительные работы вели параллельно с реконструкцией на 1-м этаже. В плане проектной документации и монтажа - самый неудачный проект. Местами не было строительной готовности. Существующий монтаж аппаратуры был не пригоден. Частично тестером линии читались какие-то шлейфы с дымовыми датчиками и ИПР-ами. Монтаж электрических проводок и кабельных конструкций нерабочий или отсутствовал. Связи между панелями не было. В сопряжении со смежными системами по узлам обвязки оборудования проектное решение отсутствовало. Имеющаяся часть монтажа по обвязке была выполнена по временной схеме навесным монтажем без защиты от механических повреждений, на скрутках без электрической изоляции. На 2-м этаже в угловом зале осталась отдельно стоящая сигналка Esser-а. Приходилось по крыше "кидать сопли" от панели к оборудованию, чтобы подать команду на сработку без обратной связи с ним. Панели были укомплектованы б/у-шными платами с разными прошивками, находившимися в отказе или частично не функционировавшими. Каждую панель приходилось восстанавливать, подключать к остальным и запускать в работу индивидуально с разной степенью трудоемкости. Работа затруднена тем, что мастами на металлических конструкциях выходит фаза электропитания или статический заряд. Часто получали удар током при касании.

Голосовое оповещение и трансляция подключались одной скруткой сзади за стойкой усилителей и всегда было откинуто, потому что сработки были постоянными из-за засоренных и несправных дымовых датчиков.

Сменные диспетчеры жаловались, что с общеобменной приточно-вытяжной вентиляцией на АРМ-е с Desigo больше половины было нарисовано, но не функционировало. Та часть вентиляции, которая работала, дула влажным воздухом, но регулировке не поддавалась и не управлялась. Отказ сбросить не возможно, так как не было отклика от аппаратуры
