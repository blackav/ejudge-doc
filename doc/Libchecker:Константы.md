Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Константы](libchecker:Константы "wikilink")

**`enum`**

`{`  
`RUN_OK = 0,`  
`RUN_PRESENTATION_ERR = 4,`  
`RUN_WRONG_ANSWER_ERR = 5,`  
`RUN_CHECK_FAILED = 6`  
`};`

Данные константы перечисляют коды завершения, доступные для проверяющей
программы. Если проверяющая программа вернёт какой-либо код возврата,
кроме указанных выше, программа run преобразует этот код возврата в код
возврата `RUN_CHECK_FAILED`.
