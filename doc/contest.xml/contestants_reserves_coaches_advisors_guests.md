Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Использование](../использование.md)/[Конфигурационные
файлы](../конфигурационные_файлы.md)/[contest.xml](../contest.xml.md)/[contestants,
reserves, coaches, advisors,
guests](contestants_reserves_coaches_advisors_guests.md)

|                          |                                                                                                                                                                                                                                                             |     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| **Имя элемента**:        | **`contestants, reserves, coaches, advisors, guests`**                                                                                                                                                                                                      |     |
| **Содержится в:**        | [`contest`](contest.md)                                                                                                                                                                                                                 |     |
| **Может содержать:**     | [`field`](field.md)                                                                                                                                                                                                                     |     |
| **Атрибуты:**            | [`min`](contestants_reserves_coaches_advisors_guests/min.md), [`max`](contestants_reserves_coaches_advisors_guests/max.md),[`initial`](contestants_reserves_coaches_advisors_guests/initial.md) |     |
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
[`min`](contestants_reserves_coaches_advisors_guests/min.md)
позволяет задать минимальное число лиц в данной категории. Например,
минимальное количество игроков одной команды (contestants) в командном
турнире может быть установлено в 2 или 3, а в личном турнире — в 1. Если
у каждого участника должен быть тренер, минимальное число лиц этой
категории (coaches) должно быть установлено в 1. Атрибут
[`max`](contestants_reserves_coaches_advisors_guests/max.md)
позволяет задать максимальное число лиц в данной категории. Например,
максимальное количество игроков одной команды в командном турнире равно
3, а в личном турнире — 1. Атрибут
[initial](contestants_reserves_coaches_advisors_guests/initial.md)
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
