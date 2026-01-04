Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[contest.xml](contest.xml.md)/[`enable_avatar`](contest.xml:enable_avatar.md)

|                            |                                             |     |
|----------------------------|---------------------------------------------|-----|
| **Имя атрибута**:          | **`enable_avatar`**                         |     |
| **Содержится в:**          | [`contest`](contest.xml:contest.md) |     |
| **Тип значения:**          | *boolean*                                   |     |
| **Может отсутствовать:**   | *да*                                        |     |
| **Значение по умолчанию:** | false                                       |     |

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"General settings (contest.xml)"*, блок *"Various contest's flags"*,
поле *"Invisible in serve-control?"*.

**Описание.** Если этот атрибут установлен в *true* или *yes*, в данном
турнире включается [поддержка аватаров](поддержка_аватаров.md).

Пример:

<contest id="auto"
          disable_team_password="yes"
          managed="yes"
          enable_avatar="yes"
          run_managed="yes">

Поддерживается с версии [3.7.0](изменения_в_версии_3.7.0.md).
