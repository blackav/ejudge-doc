Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Использование](../использование.md)/[Бот
для telegram](../бот_для_telegram.md)/[Настройка файла
ejudge.xml](_настройка_файла_ejudge.xml.md)

Бот для telegram реализован в виде плагина для ejudge и использует базу
MongoDB для хранения своего состояния.

В глобальном конфигурационном файле ejudge.xml должен быть активирован
плагин MongoDB. В раздел `<plugins>` добавьте следующие строки:

`  `<plugins>  
`    `  
`    `<plugin type="common" name="mongo" load="yes">  
`      `<config/>  
`    `</plugin>  
`  `</plugins>

Убедитесь, что плагин для MongoDB был успешно скомпилирован. В каталоге
`/opt/ejudge/libexec/ejudge/plugins` должен находиться файл
`common_mongo.so`. Если этого файла нет, то, скорее всего, при
компиляции ejudge в системе не были установлены библиотеки для клиента
MongoDB. Доустановите библиотеки и перекомпилируйте ejudge.

Добавьте конфигурацию для плагина telegram. В раздел `<plugins>`
добавьте следующие строки:

`  `<plugins>  
`    `  
`    `<plugin type="sn" name="telegram" load="yes">  
`      `<config>  
`        `<bots>  
`          `<bot>`275183432:AAHoM4qTSxTjTNV8ct0Z4pSL319oo5-JzPU`</bot>  
`        `</bots>  
`      `</config>  
`    `</plugin>  
`  `</plugins>

Cюда вписывается токен, полученный при [создании
бота](../создание_бота_для_telegram.md).

Убедитесь, что плагин для telegram был успешно скомпилирован. В каталоге
`/opt/ejudge/libexec/ejudge/plugins` должен находиться файл
`sn_telegram.so`.
