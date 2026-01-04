Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Работа
с
памятью](Libchecker:Работа_с_памятью "wikilink")/[`XMEMMOVE`](Libchecker:XMEMMOVE "wikilink")

Данный макрос является оберткой над функцией `memmove` и позволяет
копировать заданное количество элементов массива.

Например, если нужно скопировать `n` элементов из массива `src` в массив
`dst`, можно использовать XMEMMOVE:

`XMEMMOVE(dst, src, n);`

вместо вызова memmove:

`memmove(dst, src, n * sizeof(dst[0]));`

Таким образом, снижается риск забыть умножить число элементов массива на
размер одного элемента.
