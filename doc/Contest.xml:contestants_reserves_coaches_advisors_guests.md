Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[contest.xml](contest.xml "wikilink")/[contestants,
reserves, coaches, advisors,
guests](contest.xml:contestants_reserves_coaches_advisors_guests "wikilink")

|                          |                                                                                                                                                                                                                                                             |     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| **Имя элемента**:        | **`contestants, reserves, coaches, advisors, guests`**                                                                                                                                                                                                      |     |
| **Содержится в:**        | [`contest`](contest.xml:contest "wikilink")                                                                                                                                                                                                                 |     |
| **Может содержать:**     | [`field`](contest.xml:field "wikilink")                                                                                                                                                                                                                     |     |
| **Атрибуты:**            | [`min`](contest.xml:contestants_reserves_coaches_advisors_guests:min "wikilink"), [`max`](contest.xml:contestants_reserves_coaches_advisors_guests:max "wikilink"),[`initial`](contest.xml:contestants_reserves_coaches_advisors_guests:initial "wikilink") |     |
| **Тип содержимого:**     | игнорируется                                                                                                                                                                                                                                                |     |
| **Может отсутствовать:** | *да*                                                                                                                                                                                                                                                        |     |
| **Может повторяться:**   | *нет*                                                                                                                                                                                                                                                       |     |

**Описание.** Описание нескольких элементов объединено в один раздел,
так как эти элементы очень близки друг другу. Данные элементы позволяют
задавать ограничения на количество лиц соответствующей категории. Кроме
того, данные элементы содержат в себе элементы `field`, задающие поля
ввода регистрационной анкеты. Элемент `contestants` соответствует
категории игроков турнира, элемент `reserves` соответствует категории
запасных игроков, элемент `coaches` — категории тренеров, элемент
`advisors` — категории руководителей, и элемент `guests` — прочим.

Атрибут
[`min`](contest.xml:contestants_reserves_coaches_advisors_guests:min "wikilink")
позволяет задать минимальное число лиц в данной категории. Например,
минимальное количество игроков одной команды (contestants) в командном
турнире может быть установлено в 2 или 3, а в личном турнире — в 1. Если
у каждого участника должен быть тренер, минимальное число лиц этой
категории (coaches) должно быть установлено в 1. Атрибут
[`max`](contest.xml:contestants_reserves_coaches_advisors_guests:max "wikilink")
позволяет задать максимальное число лиц в данной категории. Например,
максимальное количество игроков одной команды в командном турнире равно
3, а в личном турнире — 1. Атрибут
[initial](contest.xml:contestants_reserves_coaches_advisors_guests:initial "wikilink")
позволяет задать, формы ввода для скольких лиц в данной категории будут
выведены при регистрации на турнир, когда формы печатаются для данного
пользователя первый раз.

**Пример.**

<contestants min="2" max="3">  
` `<field id="firstname" mandatory="yes"/>  
` `<field id="middlename"/>  
` `<field id="surname" mandatory="yes"/>  
` `<field id="status" mandatory="yes"/>  
` `<field id="grade" mandatory="yes"/>  
` `<field id="group"/>  
</contestants>  
<reserves min="0" max="1">  
` `<field id="firstname" mandatory="yes"/>  
` `<field id="middlename"/>  
` `<field id="surname" mandatory="yes"/>  
` `<field id="status" mandatory="yes"/>  
` `<field id="grade" mandatory="yes"/>  
` `<field id="group"/>  
</reserves>  
<coaches min="1" max="1">  
` `<field id="firstname" mandatory="yes"/>  
` `<field id="middlename"/>  
` `<field id="surname" mandatory="yes"/>  
` `<field id="status" mandatory="yes"/>  
` `<field id="occupation" mandatory="yes"/>  
</coaches>  
<advisors min="0" max="1">  
` `<field id="firstname" mandatory="yes"/>  
` `<field id="middlename"/>  
` `<field id="surname" mandatory="yes"/>  
` `<field id="status" mandatory="yes"/>  
` `<field id="occupation" mandatory="yes"/>  
</advisors>
