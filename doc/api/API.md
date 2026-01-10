Навигация: [Главная страница](../main_Page.md)/[Система ejudge](../система_ejudge.md)/[Использование](../использование.md)/[API](API.md)

## Аутентификация

Все API-методы поддерживают как аутентификацию с помощью cookie +
session, как для веб-браузера, так и аутентификацию с помощью API ключа.

API ключ создается в веб-интерфейсе мастера турнира или участника
турнира. Мастер турнира может создавать привилегированные ключи с
привязкой к турниру или без привязки к турниру, участник турнира может
создавать ключи API только для этого турнира.

### Создание привилегированного ключа API

Для создания ключа в интерфейсе администратора выберите пункт меню View
/ API Keys. Затем можно уточнить параметры создаваемого ключа в разделе
"Create new API key".

- "Duration" позволяет задать срок действия ключа. По-умолчанию он
  неограничен.
- "Contest ID" позволяет указать номер турнира, для которого действует
  ключ. Если не указать номер турнира, ключ действует для всех турниров.
- "Priv Level" позволяет задать уровень привилегий: "User" — обычный
  участнк турнира, "Observer" — наблюдатель, "Judge" — судья, "Admin" —
  администратор турнира.

Затем при нажатии на "Submit" будет создана новый ключ API.

В браузере отобразятся данные созданного ключа. Из них в текущей версии
требуется только "API key token" (это первая строка таблицы). Например,
пусть API key token равен `qUcNocRPJnK7iXE8Wm1ty6XfB5vUVVJIjSrYEmoha-c`.
Чтобы использовать токен для аутентификации в запросах, в http заголовок
нужно добавить строку:

`Authorization: Bearer AQAA`<TOKEN>

То есть перед значением токена приписывается `AQAA`.

Полная документация на API: [1](https://ejudge.ru/swagger/index.html).

Отдельные вызовы описаны далее.

## Привилегированный API

- [get-submit](priv/get-submit.md)
- [submit-run](priv/submit-run.md)
- [submit-run-input](priv/submit-run-input.md)
- [get-user](priv/get-user.md)

## Непривилегированный API

- [get-submit](unpriv/get-submit.md)
- [submit-run-input](unpriv/submit-run-input.md)

## API конфигурации (serve-control)

- [`cnts-list-session-json`](serve-control/cnts-list-session-json.md)
- [`cnts-get-value-json`](serve-control/cnts-get-value-json.md)
- [`cnts-start-edit-json`](serve-control/cnts-start-edit-json.md)
- [`cnts-forget-json`](serve-control/cnts-forget-json.md)
- [`cnts-commit-json`](serve-control/cnts-commit-json.md)
- [`cnts-dry-commit-json`](serve-control/cnts-dry-commit-json.md)
- [`cnts-check-tests-json`](serve-control/cnts-check-tests-json.md)
- [`cnts-delete-value-json`](serve-control/cnts-delete-value-json.md)
- [`cnts-set-value-json`](serve-control/cnts-set-value-json.md)
- [`cnts-minimize-problem-json`](serve-control/cnts-minimize-problem-json.md)
