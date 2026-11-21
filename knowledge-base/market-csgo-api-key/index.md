Источник: /knowledge-base/market-csgo-api-key/

# Получение API-ключа Market CS:GO

В этом руководстве описано, как войти в Market CS:GO, настроить ссылку для обмена, сгенерировать API-ключ и добавить его в PROFITON Launcher.

> **⚠️ Важно:** никому не передавайте созданный API-ключ и храните его в надёжном месте.

* * *

## Вход в Market CS:GO

1.  Откройте страницу [**https://market.csgo.com/login**](https://market.csgo.com/login). Сайт перенаправит вас на страницу входа в Steam.
2.  Введите логин и пароль от нужной учётной записи Steam.

**Скриншот: вход в учётную запись Steam**

[![Форма входа Steam Community: поля имени аккаунта и пароля, флажок запоминания и кнопка Sign in.](/images/knowledge-base/market-csgo-api-key/image1.avif)](/images/knowledge-base/market-csgo-api-key/image1.avif)

[![Подтверждение входа Steam: стрелка указывает на Enter a code instead для ввода кода вместо подтверждения в приложении.](/images/knowledge-base/market-csgo-api-key/image3.avif)](/images/knowledge-base/market-csgo-api-key/image3.avif)

3.  Введите одноразовый код Steam Guard. Посмотреть его можно в PROFITON Launcher: в таблице аккаунтов нажмите кнопку **«Ключ»** напротив нужного аккаунта.

**Скриншот: кнопка «Ключ» в PROFITON Launcher**

[![Таблица аккаунтов PROFITON Launcher: значок ключа в столбце MaFile выделен рамкой и стрелкой.](/images/knowledge-base/market-csgo-api-key/image2.avif)](/images/knowledge-base/market-csgo-api-key/image2.avif)

4.  Подтвердите авторизацию на Market CS:GO.

**Скриншот: подтверждение авторизации**

[![Страница авторизации dota2.net через Steam: стрелка выделяет кнопку Sign In выбранного аккаунта.](/images/knowledge-base/market-csgo-api-key/image4.avif)](/images/knowledge-base/market-csgo-api-key/image4.avif)

* * *

**Установка ссылки для обмена**

### 1\. Откройте настройки Market CS:GO

Перейдите на страницу [**https://market.csgo.com/ru/usercab/settings**](https://market.csgo.com/ru/usercab/settings) и нажмите кнопку **«Где найти ссылку на обмен?»**.

[![Базовые настройки Market: пустое поле ссылки обмена и выделенная подсказка «Где найти ссылку на обмен?».](/images/knowledge-base/market-csgo-api-key/image7.avif)](/images/knowledge-base/market-csgo-api-key/image7.avif)

Откроется страница Steam с вашей ссылкой для обмена.

[![Раздел Steam «Who can send me Trade Offers?»: выделены настройки приватности и поле Trade URL для копирования ссылки обмена.](/images/knowledge-base/market-csgo-api-key/image8.avif)](/images/knowledge-base/market-csgo-api-key/image8.avif)

### 2\. Проверьте приватность инвентаря

В верхней части страницы убедитесь, что приватность инвентаря установлена в режим **Public**.

[![Страница предложений обмена Steam: ссылка Edit privacy settings для изменения открытости инвентаря выделена стрелкой.](/images/knowledge-base/market-csgo-api-key/image12.avif)](/images/knowledge-base/market-csgo-api-key/image12.avif)

Если указан другой режим, нажмите **Edit privacy settings**, установите для инвентаря значение **Public** и сохраните изменения.

[![Настройки приватности Steam: для профиля My profile и инвентаря Inventory выбрано Public.](/images/knowledge-base/market-csgo-api-key/image13.avif)](/images/knowledge-base/market-csgo-api-key/image13.avif)

### 3\. Добавьте ссылку в Market CS:GO

Скопируйте ссылку Steam, вставьте её в поле **«Ссылка для обмена»** в настройках Market CS:GO и нажмите **«Подтвердить»**.

[![Подтверждение ссылки обмена в настройках Market: заполненное поле и выделенная кнопка «Подтвердить».](/images/knowledge-base/market-csgo-api-key/image9.avif)](/images/knowledge-base/market-csgo-api-key/image9.avif)

После успешной привязки обновите страницу настроек и убедитесь, что ссылка сохранилась.

[![Настройки Market: ссылка Steam для обмена сохранена, рядом доступна кнопка «Изменить».](/images/knowledge-base/market-csgo-api-key/image14.avif)](/images/knowledge-base/market-csgo-api-key/image14.avif)

### Ошибка проверки ссылки

Если после подтверждения появилась ошибка проверки ссылки:

[![Ошибка Market CS:GO при проверке ссылки обмена: бот не может забрать или передать вещи; предлагается проверить офлайн-трейды.](/images/knowledge-base/market-csgo-api-key/image10.avif)](/images/knowledge-base/market-csgo-api-key/image10.avif)

-   убедитесь, что профиль и инвентарь Steam доступны публично, затем повторите привязку
-   откройте [**https://steamcommunity.com/tradeoffer/new/?partner=1**](https://steamcommunity.com/tradeoffer/new/?partner=1). На этой странице могут быть указаны причины блокировки обменов
-   устраните указанное Steam ограничение или дождитесь окончания срока блокировки.

Например, обмены могут быть временно недоступны после длительного отсутствия активности в аккаунте или сброса пароля.

[![Сообщение Steam об ограничении обмена после сброса пароля давно неактивного аккаунта; в примере осталось 19 дней.](/images/knowledge-base/market-csgo-api-key/image11.avif)](/images/knowledge-base/market-csgo-api-key/image11.avif)

* * *

## Генерация API-ключа

1.  Перейдите на страницу [**https://market.csgo.com/ru/api/content/start#apigen**](https://market.csgo.com/ru/api/content/start#apigen).
2.  Нажмите кнопку **«Сгенерировать API ключ»**.

**Скриншот: генерация API-ключа**

[![Страница «Создание API ключа» Market: стрелками выделена кнопка «Сгенерировать API ключ».](/images/knowledge-base/market-csgo-api-key/image5.avif)](/images/knowledge-base/market-csgo-api-key/image5.avif)

3.  Если появилась ошибка **You must set up trade link first**, сначала выполните действия из раздела **«Установка ссылки для обмена»** выше.

**Скриншот: ошибка You must set up trade link first**

[![Ошибка Market «You must set up trade link first»: перед созданием ключа требуется настроить ссылку обмена.](/images/knowledge-base/market-csgo-api-key/image6.avif)](/images/knowledge-base/market-csgo-api-key/image6.avif)

4.  Если возникла ошибка проверки ссылки для обмена, попробуйте нажать кнопку генерации ключа повторно. Иногда ключ создаётся не с первой попытки.

После успешной генерации ключ отобразится на месте кнопки.

**Скриншот: созданный API-ключ**

[![Страница Market после генерации API-ключа: поле секретного ключа и кнопки журналирования запросов и белого списка IP-адресов.](/images/knowledge-base/market-csgo-api-key/image15.avif)](/images/knowledge-base/market-csgo-api-key/image15.avif)

* * *

## Добавление ключа в PROFITON Launcher

Скопируйте созданный ключ и сохраните его в надёжном месте. Затем откройте в PROFITON Launcher раздел **«Аккаунты»**, дважды нажмите на ячейку **Market CS:GO API** напротив нужного аккаунта, вставьте ключ и сохраните изменение.
