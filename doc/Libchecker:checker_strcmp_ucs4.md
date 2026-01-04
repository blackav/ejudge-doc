Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Перекодирование
текстовых
данных](Libchecker:Перекодирование_текстовых_данных "wikilink")/[`checker_strcmp_ucs4`](Libchecker:checker_strcmp_ucs4 "wikilink")

Функция сравнивает две UCS-4 строки.

`int checker_strcmp_ucs4(const int *s1, const int *s2);`

Параметр `s1` — первая сравниваемая строка. Параметр `s2` — вторая
сравниваемая строка. Значения параметров не должны быть равны `NULL`.
Обе строки должны завершаться символом с кодом 0.

Функция возвращает:

- отрицательное значение, если первая строка лексикографически меньше
  второй,
- 0, если строки равны,
- положительное значение, если первая строка лексикографически больше
  второй.

См. также:
[`checker_strcmp_ucs4_nocase`](libchecker:checker_strcmp_ucs4_nocase "wikilink").
