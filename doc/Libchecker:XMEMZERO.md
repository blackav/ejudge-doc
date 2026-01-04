Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Работа
с
памятью](Libchecker:Работа_с_памятью "wikilink")/[`XMEMZERO`](Libchecker:XMEMZERO "wikilink")

Данный макрос является оберткой над функцией `memset` и позволяет
обнулить заданное число элементов массива.

Например, если нужно обнулить `n` элементов массива `dst`, можно
использовать XMEMZERO:

`XMEMZERO(dst, n);`

вместо вызова memset:

`memset(dst, 0, n * sizeof(dst[0]));`

Таким образом, снижается риск забыть умножить число элементов массива на
размер одного элемента.
