# WarfaceBotFB 
![GitHub All Releases](https://img.shields.io/github/downloads/Lako-FC/warfacebot_fb/total?color=%231DC8EE&label=DOWNLOADS&logo=GitHub&logoColor=%231DC8EE&style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/Lako-FC/warfacebot_fb?color=%231DC8EE&label=LAST%20COMMIT&style=flat-square)
![GitHub Release Date](https://img.shields.io/github/release-date/Lako-FC/warfacebot_fb?color=%231DC8EE&label=RELEASE%20DATE&style=flat-square)
![](https://img.shields.io/badge/PRICE-free-%231DC8EE)

Группа ВК: **[Fan-Bot's ● (Fun-Bot's for Warface)][group_vk]**

Оригинальный проект: **[WarfaceBot Levak][wbl]**

Связанный проект: **[Fan-Bot's][fanbots]**

[my_vk]: https://vk.com/dlako
[group_vk]: https://vk.com/fanbots_wf
[wbl]: https://github.com/Levak/warfacebot
[wf_ru]: https://ru.warface.com/
[cygwin]: https://cygwin.com/install.html
[releases]: https://github.com/Lako-FC/warfacebot_fb/releases/
[releases_fanbots]: https://github.com/Lako-FC/warfacebot_fb/releases/
[fanbots]: https://github.com/Lako-FC/Fan-Bots

## Лицензия

В обязательном порядке необходимо понимать концепцию лицензирования и _бесплатного программного обеспечения_. Действительно, эта программа распространяется под условиями AGPLv3. Пожалуйста, найдите время, чтобы прочитать файл
**LICENSE**, который находится в пределах этого репозитория.

## Основные изменения

- GAME_HWID всегда принимает time(0).
- Изменен файл конфигурации wb.cfg -> setting_bots.ini.
- Добавлена поддержка русского языка.
- Добавлено обязательное изменение игрового профиля (статистика игрока).
- Добавлена поддержка понятия 'окончание загрузки бота'.
- Вырезано использование команды 'say'.

## Как использовать

- ### Вы должны иметь игровой аккаунт в Warface

1. Вы должны зарегистрироваться на нужном вам сервере (для RU: **[ru.warface.com][wf_ru]**). 
2. Ваш игровой аккаунт для бота должен быть свободен.
3. Вы должны понимать, что вы можете получить блокировку на данный аккаунт.

- ### Запуск бота
1. Скачайте последний релиз **Fan-Bot's** : **[Releases][releases_fanbots]**
2. Перекиньте папку 'Fan-Bot's' в удобное место.
3. Запустите 'START.exe'.
4. Выберите сервер.
5. Введите логин и пароль от игрового аккаунта, который будет ботом.
6. Нажмите 'ВОЙТИ'.

- ### Сборка бота [Windows]
1. Установите **[CygWin_x86][cygwin]**.
2. Установите необходимые зависимости :
    - Devel/make
    - Devel/gcc-core
    - Net/curl
    - Libs/zlib-devel
    - Net/libssl-devel
    - Libs/libreadline-devel
3. Загрузите из **[Releases][releases]** или данный исходный код.
4. Перенесите папку 'warfacebot_wb' в удобное место (к примеру в C:\).
5. Запустите CygWin и выполните сборку:
```bash
   $ cd "C:\warfacebot_wb\"
   $ make
```
6. После появления 'wb.exe' - сборка завершилась.
7. Далее можете скачать Fan-Bot's и заменить wb.exe на свой собранный wb.exe.

- ### Команды
- `leave`: Скажите ему, чтобы покинуть текущую игровую комнату;
- `master`: попросите его дать вам разрешения для мастера комнаты;
- `ready`: установите его в лоббистском состоянии на готово;
- `take <класс>`: ник на готов <класс-. Заставить его пройти определенный класс (медик, снайпер, инженер, стрелок);
- `follow [ник]:` Скажите ему, чтобы следовать за вами или кем-то;
- `invite [ник]`: отправить вам приглашение в комнату, в которой он находится (на случай, если вы оставили его в комнате);
- `whois <ник>`: восстановить страну и статус лобби любого подключенного игрока;
- `missions`: задачи Короны;
- `start`: если он хозяин, попробуйте завести комнату;
- `stay`: если вы находитесь в комнате, убедитесь, что вы остались, даже если комната была запущена (в течение 1 часа, пока она не покинет текущую комнату);
- `switch`: если в PvP, попробуйте сменить команду;
- `unready`: если в комнате, не готово, пока оно не получит готовый или не покинет текущую комнату.

- `create <ник>`: создать новый профиль на сервере;
- `add <ник>`: отправить на ник запрос на добавление в друзья;
- `remove <ник>`: удалить ник из списка друзей;
- `removeall`: удалить всех друзей из списка друзей;
- `open <карта/миссия>`: открыть игровую комнату с помощью «карты» (PvP) или «миссии» (PvE). Список «карта» доступен в файле src / pvp_maps.c. «Миссия» - это «тренировка», «легкий», «нормальный», «жесткий», «выживание», «зомби», «зомби-башня», «вулкан», «анубис» или «campaingnsections»;
- `name <roomname>`: изменить имя PvP-комнаты;
- `change <карта/миссия>`: изменить на «карту» или «миссия». Смотри открыто;
- `safe <карта>`: создать безопасную комнату на основе черного списка. Обратите внимание, что бот не будет отвечать на любые приглашения в безопасном режиме. Чтобы заставить его покинуть безопасный режим, используйте команду выйти;
- `channel <канал>`: переключиться на «канал»;
- `whisper <ник> <сообщение>`: отправить личное сообщение другу из клана помощник;
- `friends`: список друзей и единомышленников;
- `sleep [n]`: Зависать поток readline на 'n' секунд (1 секунда по умолчанию);
- `stats`: список всей статистики загрузки канала;
- `stay <количество> [блок]`: если в комнате, не забудьте остаться, даже если комната началась. 'count' - это количество времени, в течение которого «единица» остается (если «единица» не указана, то по умолчанию используется значение в секундах);
- `randombox [<name> <count>]`: открыть поля подсчета из случайного окна с именем name. Если ни имя, ни число не указаны, отобразите список доступных случайных коробок и их цену;
- `last <ник>`: отображение даты последнего посещения друга или клана;
- `quit`: выход из warfacebot;

- `quickplay <cmd> [arg1]`: поиск по Quickplay. 'cmd' должен быть одним из открытых, приглашать, отменять или начинать. «arg1» зависит от используемой команды:
+ `open`: 'arg1' - это PvE-миссия или PvP-карта быстрой игры;
+ `invite`: 'arg1' - ник друга;
+ `cancel`: аргументы игнорируются;
+ `start`: аргументы игнорируются.
