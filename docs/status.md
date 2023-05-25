# Статус на услугите

???- bug "Планирани профилактики"

    | Дата        | Времеви интервал | Забележка                                              |
    |:------------|:----------------:|:------------------------------------------------------:|
    | 20.06.2023  |05:30 - 6:30 EET  | Възможни са временни прекъсвания на **XMPP** услугата  |

## Регистрация на профил

| Тип               | Ограничения                               |Статус                     |
|:------------------|:-----------------------------------------:|:-------------------------:|
| Онлайн форма      |До една регистрация на час                 |![Registration Status](https://uptime.tinyserver.eu/api/badge/141/status?label=&upLabel=ОТВОРЕНА&downLabel=ЗАТВОРЕНА) |
| Инсталиран клиент |До една регистрация на час от **IP** адрес |![Registration Status](https://uptime.tinyserver.eu/api/badge/141/status?label=&upLabel=ОТВОРЕНА&downLabel=ЗАТВОРЕНА) |

## Достъпност - **XMPP**

| Показател                  |Стойност                                             |
|:---------------------------|:---------------------------------------------------:|
| Среден пинг за последните 24 часа|![Ping Average](https://uptime.tinyserver.eu/api/badge/120/ping?label=) |
| Достъпност за последните 24 часа |![Uptime 24h](https://uptime.tinyserver.eu/api/badge/121/uptime/24?label=)|
| Достъпност за последните 7 дни  |![Uptime 7 days](https://uptime.tinyserver.eu/api/badge/121/uptime/168?label=)|
| Достъпност за последните 30 дни  |![Uptime 7 days](https://uptime.tinyserver.eu/api/badge/121/uptime/720?label=)|

## Съответствие и съвместимост - **XMPP**

| Тест                 |Резултат                                                                   |
|:---------------------|--------------------------------------------------------------------------:|
| **XMPP** Съответствие| ![Compliance Test](https://compliance.conversations.im/badge/chatrix.one) |
|**SRV** Записи / Достъп| <a href='https://xmpp.love/servers/chatrix.one/results'><img src='https://xmpp.love/servers/chatrix.one/badge' width='201px' height='18px' alt='xmpp.love score'></a> |

## Достъпност - Интернет страница

| Показател                  |Стойност                                             |
|:---------------------------|:---------------------------------------------------:|
| Среден пинг за последните 24 часа|![Ping Average](https://uptime.tinyserver.eu/api/badge/135/ping?label=) |
| Достъпност за последните 24 часа |![Uptime 24h](https://uptime.tinyserver.eu/api/badge/135/uptime/24?label=)|
| Достъпност за последните 7 дни  |![Uptime 7 days](https://uptime.tinyserver.eu/api/badge/135/uptime/168?label=)|
| Достъпност за последните 30 дни  |![Uptime 7 days](https://uptime.tinyserver.eu/api/badge/135/uptime/720?label=)|

## Технически данни

### XMPP Сървър

| Параметър            | Стойност                       |
|:---------------------|:------------------------------:|
| Процесор             | ARM Ampere                     |
| Оперативна памет     | 12GB                           |
| Дисково пространство | 64GB                           |
| Файлова система      | ext4                           |
| Операционна система  | Ubuntu 22.04 (Jammy Jellyfish) |
| Ejabberd версия      | 23.1.0                         |
| Архивиране           | Ежеседмично                    |
| Локация              | Швейцария                      |

### Бекъп сървър

| Параметър            | Стойност                       |
|:---------------------|:------------------------------:|
| Процесор             | AMD EPYC 3251                  |
| Оперативна памет     | 64GB                           |
| Дисково пространство | 5TB                            |
| Файлова система      | ZFS (RAIDZ-1)                  |
| Операционна система  | Debian 11 (Bullseye)           |
| Локация              | България                       |

## Информация за настъпили инциденти

!!! abstract "Инциденти"

    Към момента няма документирани инциденти.

## История на актуализациите

### 26.04.2023

Обновяване на Ejabberd до версия [23.04](https://github.com/processone/ejabberd/releases/tag/23.04).

- Много подобрения в **SQL** базата данни
- Ново: `mod_mam` поддръжка на **[XEP-0425: Message Moderation](https://xmpp.org/extensions/xep-0425.html)**
- Ново: `mod_muc_rtbl` поддръжка на **Real-Time Block List for MUC rooms**

### 20.01.2023

Обновяване на Ejabberd до версия [23.01](https://github.com/processone/ejabberd/releases/tag/23.01).

- Ново: Отворена е регистрацията, посредством онлайн формата или инсталиран клиент, защитена чрез **CAPTCHA** предизвикателство

### 30.10.2022

Обновяване на Ejabberd до версия [22.10](https://github.com/processone/ejabberd/releases/tag/22.10).
