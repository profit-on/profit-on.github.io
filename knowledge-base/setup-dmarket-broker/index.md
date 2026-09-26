Источник: /knowledge-base/setup-dmarket-broker/

# Настройка DMarket брокер

## Теоретические основы

**DMarket брокер** — софт для покупки и передачи игровых предметов с установленным вами процентом доходности с Торговой площадки DMarket на ваш аккаунт Steam.

Предупреждение:

**⚠️ _Важное предупреждение!_ _Использование индивидуального прокси из России (RUS) и Беларуси (BY) для аккаунтов, работающих с DMarket брокером, строго запрещено. Индивидуальный прокси настраивается в SSA — убедитесь, что выбран IP не из указанных стран, иначе DMarket может заблокировать аккаунт._**

## Практическая настройка

Примечание:

**При необходимости вы можете вернуться к исходной конфигурации. Для этого в окне редактирования конфигурации нажмите правой кнопкой мыши и выберите пункт «Вернуть шаблонную конфигурацию».**

Примечание:

В конфигурации используются два типа прокси. **Индивидуальный прокси** — выделенный IP-адрес, через который аккаунт Steam выполняет всю торговую работу (листинги, ордера на покупку, трейды). Оптимально один аккаунт на один IP, если аккаунтов много — допустимо до 2-3 на один адрес, но чем больше аккаунтов делят IP, тем выше суммарная нагрузка запросами и риск блокировки адреса со стороны Steam (ошибка 429, слишком много запросов). **Прокси-пул** (Webshare) — отдельный пул IP-адресов, который софты используют для многопоточного парсинга цен по всем торговым площадкам, работает полностью независимо от аккаунтов Steam и не расходует их лимиты запросов. Как выбрать и проверить прокси, описано в разделе [_**Прокси**_](/knowledge-base#%D0%BF%D1%80%D0%BE%D0%BA%D1%81%D0%B8) базы знаний.

**Параметры, требующие заполнения**

```
telegram:
# Токен вашего Телеграм-бота (Обязательное поле).
  token:
# Ваш чат ID в Телеграме (Обязательное поле).
  chat_id:
# Язык всех сообщений и кнопок Телеграм-бота (ru - русский, en - английский).
  language: ru
```

“Токен Telegram-бота” - уникальный ключ, который выдается при создании бота. Создайте бота через _@BotFather_ и скопируйте токен.

-   Откройте мессенджер Telegram на своем устройстве (смартфон, планшет или компьютер).
-   В поисковой строке Telegram найдите аккаунт _@BotFather ([https://t.me/BotFather](https://t.me/BotFather))_. Он является официальным сервисом для создания и настройки ботов.
-   Откройте диалог с _@BotFather_ и начните общение с ним, нажав кнопку _“Start”_ или отправив команду _/start_.
-   Для создания нового бота отправьте команду _/newbot_.
-   Следуйте инструкциям _@BotFather_:
    -   Введите имя вашего бота. Это отображаемое имя, которое видят пользователи.
    -   Введите уникальное имя пользователя для бота. Оно должно заканчиваться на «_bot_» или «_\_bot_» и быть уникальным в рамках всей платформы Telegram.
-   Если все введенные данные корректны, _@BotFather_ создаст вашего бота и предоставит вам его токен доступа. Этот токен является ключом для управления ботом и обязателен для настройки и использования бота. Сохраните его в безопасном месте.

Предупреждение:

**Для каждого софта обязательно создайте отдельного Telegram-бота. Нарушение этого правила приведёт к некорректной работе и ошибкам.**

_**“Chat ID”**_ - идентификатор вашего чата в Телеграме.

-   Откройте мессенджер Telegram на своем устройстве (смартфон, планшет или компьютер).
-   В поисковой строке Telegram найдите аккаунт _@getmyid\_bot ([https://t.me/getmyid\_bot](https://t.me/getmyid_bot))_.
-   Откройте диалог с _@getmyid\_bot_ и начните общение с ним, нажав кнопку _“Start”_ или отправив команду _/start_.
-   Если все сделано корректно, бот предоставит ваш Chat ID.

**«Language»** задаёт язык всех сообщений и кнопок Telegram-бота. Укажите _ru_ для русского языка или _en_ для английского.

```
accounts:
    - steam_id:
    - steam_id:
```

_“Accounts”_ — список SteamID аккаунтов, которые будут использоваться софтом. Необходимая информация (индивидуальный прокси, MaFile и т.д.) будет автоматически подтянута из раздела _“Аккаунты”_ в Steam Server-Side Authenticator.

```
sources:
    - (http)
```

_“Прокси-пул”_ - набор прокси-серверов для парсинга цен, не нагружает индивидуальные прокси ваших аккаунтов и не взаимодействует с аккаунтами Steam.

-   После покупки прокси-пула, вам будет предоставлена ссылка на список прокси-серверов.
-   Добавьте полученную ссылку в соответствующее поле конфигурации софта.

Примечание:

Прокси-пул приобретается на Webshare согласно [_**руководству по покупке**_](/knowledge-base/proxy-guide). Если у вас нет зарубежной карты, зарегистрируйтесь и предоставьте нам логин и пароль.

```
trade_token:
```

_“Trade\_token”_ - токен для повышения производительности софта и получения лучших лимитов на [_Dmarket.com_](http://Dmarket.com). **Актуальный токен позволяет увеличить скорость работы софта в 25 раз, так как лимиты для авторизованных пользователей значительно выше.**

-   Установите расширение [_Cookie Editor_](https://chrome.google.com/webstore/detail/cookie-editor/iphcomljdfghbkdcfndaijbokpgddeno) для вашего браузера (или аналогичное).
-   Авторизуйтесь на сайте [_Dmarket.com_](http://Dmarket.com).
-   Откройте расширение Cookie Editor и найдите куки для домена “[_dmarket.com_](http://dmarket.com)”.
-   Найдите параметр _“dm-trade-token_” и скопируйте его значение.
-   Вставьте скопированное значение в поле _“Trade\_token”_ конфигурации софта.

Предупреждение:

**Важно!!! Рекомендуется обновлять “_trade\_token_” несколько раз в месяц. Периодическая проверка и обновление токена обеспечивает стабильность работы софта.**

```
public_key:
private_key:
```

_“Public KEY и Private KEY”_ - ключи доступа к вашему аккаунту на [_Dmarket.com_](http://Dmarket.com) через API.

-   Перейдите на сайт [_Dmarket.com_](http://Dmarket.com) и авторизуйтесь.
-   Зайдите в раздел “_**Настройки аккаунта**_” (см. изображение ниже).

[![Меню профиля DMarket с пунктами «Баланс», «История», «Настройки аккаунта», «Партнёрская программа» и «Подписка».](/images/knowledge-base/dmarket-broker/image3.avif)](/images/knowledge-base/dmarket-broker/image3.avif)

-   Выберите опцию “_**Торговый API**_” (см. изображение ниже).

[![Раздел «Торговый API» в настройках DMarket: открытый и закрытый ключи, кнопки удаления и генерации ключей.](/images/knowledge-base/dmarket-broker/image0.avif)](/images/knowledge-base/dmarket-broker/image0.avif)

-   Скопируйте ключи доступа _Public KEY_ **и** _Private KEY_.

Пожалуйста, обратите внимание, что API-ключ является чувствительной информацией и не должен передаваться третьим лицам. Будьте внимательны при работе с API-ключами.

**Пример корректно заполненной конфигурации**

```
telegram:
# Токен вашего Телеграм-бота (Обязательное поле).
  token: 6352854634:SYG783ifdiUhsuIUWkekiwuHUQ24w-GQT45
# Ваш чат ID в Телеграме (Обязательное поле).
  chat_id: 2365344527
# Язык всех сообщений и кнопок Телеграм-бота (ru - русский, en - английский).
  language: ru

# Список ID игр, предметы из которых будут покупаться (730 - CS:GO, 570 - Dota 2, 252490 - Rust).
# Ключи в bindings: a8db соответствует CS:GO, 9a92 соответствует Dota 2, rust соответствует Rust.
bindings: {9a92: 570, rust: 252490, a8db: 730}
# Коэффициент смещения цены покупки.
# -1: предметы будут покупаться по цене автопокупки Steam;
#  0: предметы будут покупаться по средней цене между автопокупкой и рыночной ценой;
#  1: предметы будут покупаться по рыночной цене Steam.
estimates: {price_offset: 0.25}

feature_defaults:
# Включение/отключение возможности покупки предметов напрямую у других пользователей (true/false).
  p2p_feature_mode_enabled: true
# Включение/отключение автоматического вывода предметов с ботов DMarket (true/false).
  autowithdraw_feature_mode_enabled: true

filters:
# Диапазон цен предметов для покупки (в долларах).
  price: {lo: 0.04, hi: 50}
# Минимальный процент прибыли с учетом комиссии торговой площадки Steam [0.5 = 50%].
# Процент дохода с учётом времени разблокировки предметов (до 7 дней) на ботах Dmarket.
# Если хотя бы один раз изменить проценты через Телеграм-бот, значения из лаунчера будут игнорироваться!
  profit_days: {0: 0.4, 1: 0.42, 2: 0.44, 3: 0.46, 4: 0.48, 5: 0.5, 6: 0.52, 7: 0.54}
# Минимальное количество продаж в день на Торговой площадке Steam.
  daily_volume: 5
# Минимальная история продаж (в днях)
  min_sale_history_days: 365
# Минимальное количество выставленных предметов на Торговой площадке Steam.
  onsale_volume: 40
# Максимальное количество одинаковых предметов на один аккаунт Steam.
  duplicate_limit: 5
# Максимальное количество одинаковых предметов на всех аккаунтах.
  duplicates_limit: 7
# Минимальное количество выставленных ордеров на покупку на Торговой площадке Steam.
  buyorders_volume: 5
# Фильтр для отсеивания переоцененных предметов. Коэффициент соотношения рыночной цены и ордера на покупку.
  prices_diff_percent_limit: 0.27
# Черный список по типу предметов (только для CS2).
  items_blacklist: ["Souvenir", "Sticker", "Container", "Knife", "Graffiti", "Music Kit", "Patch", "Collectible", "Pass", "Charm"]
# Черный список по коллекциям (только для CS2).
  set_blacklist: ["The Train 2025 Collection", "The Ascent Collection", "The Boreal Collection", "The Radiant Collection", "The Fever Collection"]


# Список предметов, исключённых из покупки (формат: Название предмета:::ID игры).
  excludes:
    - Artificer's Hammer:::570
    - Artificer's Chisel:::570
    - Master Artificer's Hammer:::570
    - Genuine Weather Spring:::570
    - Genuine Weather Ash:::570
    - Genuine Weather Moonbeam:::570
    - Genuine Weather Sirocco:::570
    - Genuine Weather Aurora:::570
    - Genuine Weather Snow:::570
    - Genuine Weather Rain:::570
    - Genuine Weather Harvest:::570
    - Genuine Weather Pestilence:::570
    - Desert Eagle | Heat Treated:::730
    - XM1014 | Solitude:::730
    - Fever Case:::730

dmarket:
# Список аккаунтов Steam в формате SteamID + trade_token + public_key + private_key (обязательное поле).
  accounts:
# Шаблон
#    - steam_id: 76561198000000000
#      trade_token: xjpO7DwGcAIAxIHYIiOsYRjwVOjEZsjkiQMzs4YET0wJjiWwIMjMiycj91IWNk2JhiUzW6-iU2OIFkXIiLzGVZSMQMczSUYEEy5NN7GzmJEtYJOOPpwehjiZiMUDuAyYw7iiAzTplY6xDNhI9Uik5hI3TT4Q2UxtMcN0IIDMmy4yIhmMiccGntNihi24NXyQgNzz1TMgjZsdRFYmWiJWjNiDfOzW6dqQhUNsTcMWZZdBFNey0ITwVEWN1gV.wCg3MmjzM3QZ4YOcjOMMNIxzWY43CIkNhvmjxrw3GtkI02RwjrZ1k.zq1TiRSN2TzKIRMWM3jZhT1iMMFY6iMJtT23XlYNwsLVjzTNCMWM2L1iLiqki0BTjhHayiYZWCkeTMT1mCyY9IMdRmlBiwNnCS4RwT0mlT6ViAIAcOGYIiNMDIbcOQh11fE2jp2m1oRIkDkMh2JZNNFwdifjn9DNcNyYdMnjhNt0XM7LLYx3EYlNCgR6HMIOMXZjQwM2H1ZCYil8ILTAY2xJXl1ThlIImWafjWmuEDW5dFzMjibYOOIiTyRIQ4WVZYiYMJYII5h1ZJj1IylwCN4tziriMy2YZQTXAzmCzdQre1UzYLMLMIGVYCs5YcloIhTtzNRMlZjTBqMxRaJf5DCT7J4JZ93kmF1LEQWzciokjdDN2aZ22ELJWMYO
#      public_key: dnOa02Ocffi762L700MSb1dTb6fbbbEcjzESBQAPMkbNIcm6c27uwdGhhqwqqy11
#      private_key: ejfCLQbJcfe3c77fffaO2SAfCpGD7w75D3e6iuktkmfjIf632Lf7E9tV6drd7famNJl8XX8Ihh7vkvlmL7fGqI62bLW32ala7kvaf2ef2caa6bf8bfb2fc0ec0070bc3
# Аккаунт 1
    - steam_id: 76561199083114143
      trade_token: xjpO7DwGcAIAxIHYIiOsYRjwVOjEZsjkiQMzs4YET0wJjiWwIMjMiycj91IWNk2JhiUzW6-iU2OIFkXIiLzGVZSMQMczSUYEEy5NN7GzmJEtYJOOPpwehjiZiMUDuAyYw7iiAzTplY6xDNhI9Uik5hI3TT4Q2UxtMcN0IIDMmy4yIhmMiccGntNihi24NXyQgNzz1TMgjZsdRFYmWiJWjNiDfOzW6dqQhUNsTcMWZZdBFNey0ITwVEWN1gV.wCg3MmjzM3QZ4YOcjOMMNIxzWY43CIkNhvmjxrw3GtkI02RwjrZ1k.zq1TiRSN2TzKIRMWM3jZhT1iMMFY6iMJtT23XlYNwsLVjzTNCMWM2L1iLiqki0BTjhHayiYZWCkeTMT1mCyY9IMdRmlBiwNnCS4RwT0mlT6ViAIAcOGYIiNMDIbcOQh11fE2jp2m1oRIkDkMh2JZNNFwdifjn9DNcNyYdMnjhNt0XM7LLYx3EYlNCgR6HMIOMXZjQwM2H1ZCYil8ILTAY2xJXl1ThlIImWafjWmuEDW5dFzMjibYOOIiTyRIQ4WVZYiYMJYII5h1ZJj1IylwCN4tziriMy2YZQTXAzmCzdQre1UzYLMLMIGVYCs5YcloIhTtzNRMlZjTBqMxRaJf5DCT7J4JZ93kmF1LEQWzciokjdDN2aZ22ELJWMYO
      public_key: dnOa02Ocffi762L700MSb1dTb6fbbbEcjzESBQAPMkbNIcm6c27uwdGhhqwqqy11
      private_key: ejfCLQbJcfe3c77fffaO2SAfCpGD7w75D3e6iuktkmfjIf632Lf7E9tV6drd7famNJl8XX8Ihh7vkvlmL7fGqI62bLW32ala7kvaf2ef2caa6bf8bfb2fc0ec0070bc3
# Аккаунт 2
    - steam_id: 76567643082655732
      trade_token: kqLm9RwGcAIAxIHYIiOsYRjwVOjEZsjkiQMzs4YET0wJjiWwIMjMiycj91IWNk2JhiUzW6-iU2OIFkXIiLzGVZSMQMczSUYEEy5NN7GzmJEtYJOOPpwehjiZiMUDuAyYw7iiAzTplY6xDNhI9Uik5hI3TT4Q2UxtMcN0IIDMmy4yIhmMiccGntNihi24NXyQgNzz1TMgjZsdRFYmWiJWjNiDfOzW6dqQhUNsTcMWZZdBFNey0ITwVEWN1gV.wCg3MmjzM3QZ4YOcjOMMNIxzWY43CIkNhvmjxrw3GtkI02RwjrZ1k.zq1TiRSN2TzKIRMWM3jZhT1iMMFY6iMJtT23XlYNwsLVjzTNCMWM2L1iLiqki0BTjhHayiYZWCkeTMT1mCyY9IMdRmlBiwNnCS4RwT0mlT6ViAIAcOGYIiNMDIbcOQh11fE2jp2m1oRIkDkMh2JZNNFwdifjn9DNcNyYdMnjhNt0XM7LLYx3EYlNCgR6HMIOMXZjQwM2H1ZCYil8ILTAY2xJXl1ThlIImWafjWmuEDW5dFzMjibYOOIiTyRIQ4WVZYiYMJYII5h1ZJj1IylwCN4tziriMy2YZQTXAzmCzdQre1UzYLMLMIGVYCs5YcloIhTtzNRMlZjTBqMxRaJf5DCT7J4JZ93kmF1LEQWzciokjdDN2aZ22ELJWMYO
      public_key: pmXb47Ocffi762L700MSb1dTb6fbbbEcjzESBQAPMkbNIcm6c27uwdGhhqwqqy11
      private_key: qkTmRWbJcfe3c77fffaO2SAfCpGD7w75D3e6iuktkmfjIf632Lf7E9tV6drd7famNJl8XX8Ihh7vkvlmL7fGqI62bLW32ala7kvaf2ef2caa6bf8bfb2fc0ec0070bc3
# Убедитесь, что все поля аккаунтов заполнены. Незаполненные аккаунты необходимо удалить!
# Добавляйте аналогично любое количество аккаунтов, следуя шаблону.
# Индивидуальный прокси и MaFile подтягиваются автоматически из Steam Server-Side Authenticator.

proxy:
# Ссылка на пул прокси (обязательное поле).
# Пример формата: - (http) https://proxy.webshare.io/api/v2/proxy/list/download/dvjevsscsqmeywegdjobpllxyuqxeqwrmyluv/-/any/username/direct/-/
  sources:
    - (http) https://proxy.webshare.io/api/v2/proxy/list/download/dvjevsscsqmeywegdjobpllxyuqxeqwrmyluv/-/any/username/direct/-/
```

### **Инструкция по использованию**

1.  В полях конфигурации софта укажите: _**SteamID, Trade\_token, Public KEY, Private KEY**_, ссылку на прокси-пул, Telegram-бота и язык бота (_**language**_). Индивидуальный прокси и MaFile подтягиваются автоматически из Steam Server-Side Authenticator.
    
2.  После внесения изменений, закройте окно настроек. Вам будет предложено сохранить конфигурацию. Выберите “Да”, чтобы применить ваши настройки.
    
3.  Активируйте привязанный Telegram-бот, нажав _Start_.
    
    ⚠️ **Уведомления о покупках будут приходить только после активации бота.**
    
4.  Запустите **DMarket брокер** в лаунчере PROFITON или через Telegram-бота.
    
    **После успешного подключения вы получите сообщение вида: _“✅ Аccount (#XXXX) connected!”_. Уведомлений должно быть столько, сколько у вас аккаунтов.**
    
    [![Уведомление Telegram-бота об успешном подключении аккаунта.](/images/knowledge-base/dmarket-broker/image1.avif)](/images/knowledge-base/dmarket-broker/image1.avif)
    
5.  Уведомления о покупках будут приходить в Telegram-бот, в том числе и данные о прибыли.
    

### **Настройка аккаунта и активация сделок P2P**

1.  Перейдите в “_**Настройки аккаунта**_” на [_**Dmarket.com**_](http://dmarket.com/) и выберите “_**Steam аккаунт**_”.
    
    [![Пункт «Steam аккаунт» в настройках DMarket.](/images/knowledge-base/dmarket-broker/image2.avif)](/images/knowledge-base/dmarket-broker/image2.avif)
    
2.  Заполните необходимые параметры для сделок с ботами DMarket и включите сделки P2P.
    
    ⚠️ **По умолчанию, сделки P2P и автовывод включены.** Вы можете их настроить в софте или через Telegram-бота кнопками **⚙️ P2P** и **⚙️ Автовывод**.
    

**Когда нужен перезапуск**

-   **Изменили конфигурацию** → перезапустите DMarket брокер.
-   **Добавили, удалили или изменили аккаунт** → перезапустите **все** софты с этим аккаунтом.
-   **Сменили индивидуальный прокси** → обновите в SSA, перезапустите **все** софты с этим аккаунтом. Например, если не перезапустить Steam Market селлер и Market CS:GO брокер, они продолжат работать через старый IP.
-   **Сменили прокси-пул** (Webshare) → обновите в софтах, где он указан (например, Steam Market селлер, Market CS:GO брокер), и перезапустите их. В SSA прокси-пул не настраивается.
-   **Сменили пароль Steam или API-ключ Market CS:GO** → перезапустите все софты с этим аккаунтом.

Примечание:

Если открыли конфигурацию, ничего не изменили — перезапуск не нужен.
