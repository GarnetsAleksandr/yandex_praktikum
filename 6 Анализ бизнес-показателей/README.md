# [Анализ бизнес-показателей](https://github.com/GarnetsAleksandr/yandex_praktikum/blob/main/6%20%D0%90%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D0%B1%D0%B8%D0%B7%D0%BD%D0%B5%D1%81-%D0%BF%D0%BE%D0%BA%D0%B0%D0%B7%D0%B0%D1%82%D0%B5%D0%BB%D0%B5%D0%B9/garnets_m2_p2_v3.ipynb)


## Описание проекта

Вы — маркетинговый аналитик развлекательного приложения Procrastinate Pro+. Несмотря на огромные вложения в рекламу, последние несколько месяцев компания терпит убытки. Ваша задача — разобраться в причинах и помочь компании выйти в плюс.

Есть данные о пользователях, привлечённых с 1 мая по 27 октября 2019 года:
- лог сервера с данными об их посещениях,
- выгрузка их покупок за этот период,
- рекламные расходы.

Вам предстоит изучить:

- откуда приходят пользователи и какими устройствами они пользуются,
- сколько стоит привлечение пользователей из различных рекламных каналов;
- сколько денег приносит каждый клиент,
- когда расходы на привлечение клиента окупаются,
- какие факторы мешают привлечению клиентов.


## Описание данных

В вашем распоряжении три датасета. Файл visits_info_short.csv хранит лог сервера с информацией о посещениях сайта, orders_info_short.csv — информацию о покупках, а costs_info_short.csv — информацию о расходах на рекламу.

**Структура visits_info_short.csv**

- User Id — уникальный идентификатор пользователя,
- Region — страна пользователя,
- Device — тип устройства пользователя,
- Channel — идентификатор источника перехода,
- Session Start — дата и время начала сессии,
- Session End — дата и время окончания сессии.

**Структура orders_info_short.csv**

- User Id — уникальный идентификатор пользователя,
- Event Dt — дата и время покупки,
- Revenue — сумма заказа.

**Структура costs_info_short.csv**

- Channel — идентификатор рекламного источника,
- Dt — дата проведения рекламной кампании,
- Costs — расходы на эту кампанию.

## Вывод

Причины убытков компании: Основная причина убытков - Реклама не окупается. ROI в конце 2й недели — чуть выше 80%. Общий САС увеличивается. На LTV влияет сезонный фактор, но и этот показатель достаточно стабилен. Значит, дело не в ухудшении качества пользователей.

Начнем с разбивки по странам. Вот что говорят графики:

Реклама не окупается только в США, в европе окупаемость примерно одинаковая и равна 150%
САС в европе стабилен, в то время как в США постоянно растет.
LTV всё так же подвержен сезонности, но стабилен.
Рассмотрим графики с разбивкой по каналам привлечения: Из всех источников привлечения, не окупаются 3 канала это FaceBoom AdNonSense и TipTop Расходы на каналы TipTop и FaceBoom постоянно ростут, gри этом САС канала TipTop так же растет.

Окупаются только пользователи РС, при этом у нх чуть выше удержание. У пользователей эпл самая низкая окупаемость. Возможно стоит перераспределить бюджет в сторону РС, получая более качественных пользователей.

Причины плохой окупаемости

TipTop и FaceBoom -постоянный рост затрат на рекламу
TipTop - постоянный рост САС
FaceBoom и AdNonSense - самое низкое удержание платящих клиентов
Низкое удержание платящих пользователей в США
Низкая конверсия пользователей в европе
Низкая конверсия пользователей РС
Низкая окупаемость пользователей эпл
Рекомендации

Положительная окупаемость в европе и стабильный САС- признак правильного направления развития.
Следует уменьшить затраты на рекламу в США
Снизить затраты или полностью уйти с площадки TipTop
Увеличить удержание на площадках FaceBoom и AdNonSense
Уделить больше внимания рекламе на РС
