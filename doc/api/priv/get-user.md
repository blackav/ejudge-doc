Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[API](API "wikilink")/[get-user
(привилегированный)](API:priv:get-user "wikilink")

Запрос возвращает информацию о пользователе.

Уровень доступа: администратор в контесте (аутентификация с помощью API
key или EJSID/session_id).

Method: `GET`

Параметры:

- `contest_id` (int) - идентификатор турнира
- `other_user_id` (int) - идентификатор турнира
- `other_user_login` (string) - идентификатор турнира
- `action` (string) - строка get-user

Response content type: `application/json`

В случае ошибки возвращается JSON и устанавливается статус http-запроса.

`{`  
`  "ok": false,`  
`  "server_time": UNIX-TIMESTAMP,`  
`  "action": "get-submit",`  
`  "error": {`  
`    "num": ERROR-CODE,`  
`    "symbol": ERROR-SYMBOL`  
`  }`  
`}`

В случае успеха возвращается JSON:

`{`  
`  "ok": true,`  
`  "result": {`  
`    "submit_id": ID,`  
`    "user_id": USER-ID,`  
`    "prob_id": PROB-ID,`  
`    "lang_id": LANG-ID,`  
`    "ext_user_kind": EXT-USER-KIND,`  
`    "ext_user": EXT-USER,`  
`    "notify_driver": NOTIFY-DRIVER,`  
`    "notify_kind" : NOTIFY-KIND,`  
`    "notify_queue" : NOTIFY-QUEUE,`  
`    "status": STATUS,`  
`    "status_str": STATUS-SHORT-STR,`  
`    "compiler_output": COMPILER-MESSAGES,`  
`    "test_checker_output": TEST-CHECKER-MESSAGES,`  
`    "time": CPU-TIME,`  
`    "real_time": REAL-TIME,`  
`    "exit_code": PROCESS-EXIT-CODE,`  
`    "term_signal": TERMINATION-SIGNAL,`  
`    "max_memory_used": VIRT-MEM-USE,`  
`    "max_rss": MEMORY-USE,`  
`    "input": INPUT,`  
`    "output": OUTPUT-TEXT,`  
`    "error": ERROR-TEXT`  
`  }`  
`}`

Поля `ext_user_kind`, `ext_user` содержат [внешний идентификатор
пользователя](Внешние_идентификаторы_пользователей "wikilink")
([3.11.0](Изменения_в_версии_3.11.0 "wikilink")), если он был установлен
при отправке посылки.

Поля `notify_driver`, `notify_kind`, `notify_queue` содержат
[идентификатор очереди
сообщений](Нотификации_во_внешние_системы "wikilink")
([3.11.0](Изменения_в_версии_3.11.0 "wikilink")), если он был установлен
при отправке посылки.

Пример кода на python:

`import requests`  
`import os`  
`import urllib.parse`  
  
`URL = '`[`http://HOST/cgi-bin/master`](http://HOST/cgi-bin/master)`'`  
`TOKEN = 'TOKEN'`  
`CONTEST_ID = 1`  
`SUBMIT_ID = 50`  
  
`headers = {`  
`        "Authorization": "Bearer AQAA" + TOKEN`  
`}`  
  
`data = {`  
`        "contest_id" : CONTEST_ID,`  
`        "json" : 1,`  
`        "action" : "get-submit",`  
`        "submit_id" : SUBMIT_ID,`  
`}`  
`response = requests.get(URL+"?"+urllib.parse.urlencode(data), headers=headers)`  
`print(response.json())`

Поддерживается начиная с версии
[3.13.0](изменения_в_версии_3.13.0 "wikilink").
