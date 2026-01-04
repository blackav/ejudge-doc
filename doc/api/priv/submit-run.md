Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[API](API.md)/[submit-run
(привилегированный)](API:priv:submit-run.md)

Запрос отправляет на проверку файл с исходным кодом.

Уровень доступа: администратор в контесте (аутентификация с помощью API
key или EJSID/session_id).

Method: `POST`

Content-type: `multipart/form-data`

Параметры:

- `contest_id` (int) - идентификатор турнира
- `action` (string) — строка `submit-run`.
- `sender_user_login` (string, optional) — логин пользователя, от имени
  которого выполняется посылка.
- `sender_user_id` (int, optional) — user id пользователя (если не задан
  sender_user_login).
- `sender_ip` (string, optional) — IP-адрес отправителя.
- `sender_ssl_flag` (int, optional) — 1, если протокол HTTPS; 0, если
  HTTP.
- `problem_uuid` (uuid, \*) — UUID задачи, если присутствует, то поиск
  задачи выполняется по UUID.
- `problem_name` (string, \*) — либо short_name задачи, либо
  internal_name задачи.
- `problem` (int, \*) — id задачи.
- `variant` (int, optional) — вариант задачи.
- `language_name` (string, \*\*) — короткое имя (short_name) языка
  программирования.
- `lang_id` (int, \*\*) — либо id (int) языка программирования либо
  короткое имя (string) языка программирования.
- `eoln_type` (int, optional) — тип преобразования концов строк.
- `is_visible` (int, optional) — если значение \> 0, посылка не будет
  "невидимой".
- `file` (string, \*\*\*) — исходный код программы.
- `text_form` (string, \*\*\*) — исходный код программы (альтернатива
  для file).
- `not_ok_is_cf` (int, optional) — если значение положительно, любой
  не-OK вердикт по этой посылке будет рассматриваться как Check Failed
  ([3.10.1](Изменения_в_версии_3.10.1.md)).
- `rejudge_flag` (int, optional) — если значение положительно,

посылка будет тестироваться с пониженным приоритетом, как при
перетестировании ([3.10.1](Изменения_в_версии_3.10.1.md)).

- `ext_user_kind`, `ext_user` — [внешний идентификатор
  пользователя](Внешние_идентификаторы_пользователей.md)
  ([3.11.0](Изменения_в_версии_3.11.0.md)).
- `notify_driver`, `notify_kind`, `notify_queue` — [идентификатор
  очереди сообщений](Нотификации_во_внешние_системы.md)
  ([3.11.0](Изменения_в_версии_3.11.0.md)).

Из параметров `problem_uuid`, `problem_name`, `problem` должен быть
указан только один.

Из параметров `language_name`, `lang_id` должен быть указан только один.

Из параметров `file`, `text_form` должет быть указан только один.

Response content type: `application/json`

В случае ошибки возвращается JSON:

`{`  
`  "ok": false,`  
`  "server_time": UNIX-TIMESTAMP,`  
`  "action": "submit-run",`  
`  "error": {`  
`    "num": ERROR-CODE,`  
`    "symbol": ERROR-SYMBOL,`  
`    "message": ERROR-MESSAGE`  
`  }`  
`}`

В случае успеха возвращается JSON:

`{`  
`  "ok": true,`  
`  "result": {`  
`    "run_id": ID,`  
`    "run_uuid": UUID`  
`  }`  
`}`
