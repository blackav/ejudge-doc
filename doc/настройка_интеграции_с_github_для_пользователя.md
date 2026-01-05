Навигация: [Главная страница](main_Page.md)/[Система
ejudge](система_ejudge.md)/[Использование](использование.md)/[Интеграция
с github/gitlab](Интеграция_с_github/gitlab.md)/[Настройка
интеграции с github для
пользователя](настройка_интеграции_с_github_для_пользователя.md)

Чтобы ejudge мог склонировать исходный код из репозитория, потребуется
ключ ssh. Можно использовать существующий, который используется для
других целей, но предпочтительнее сгенерировать новую пару из приветного
и публичного ключа специально для использования ejudge. Такой ключ
называется deploy key. Один и тот же deploy key можно использовать и для
github, и для gitlab интеграции.

#### Генерация ключа

Сгенерировать пару ключей можно с помощью команды
`ssh-keygen -t ed25519 -f ej_deploy`. Passphrase нужно оставить пустым.
При исполнении команды на стандартный поток вывода будет примерно
следующий вывод:

`$ ssh-keygen -t ed25519 -f ej_deploy`  
`Generating public/private ed25519 key pair.`  
`Enter passphrase (empty for no passphrase): `  
`Enter same passphrase again: `  
`Your identification has been saved in ej_deploy`  
`Your public key has been saved in ej_deploy.pub`  
`The key fingerprint is:`  
`SHA256:MZcQPKClDzn4AcM+S2tBiIJLgWKMciwxK1tj38nMs9k cher@fedora`  
`The key's randomart image is:`  
`+--[ED25519 256]--+`  
`|O*+   ooo.       |`  
`|@*=+ =  o. .     |`  
`|O*= B   o.o      |`  
`|o+=+ X . +       |`  
`|.. =o O S        |`  
`|  +    =         |`  
`| .    o E        |`  
`|                 |`  
`|                 |`  
`+----[SHA256]-----+`

В итоге в текущем каталоге появятся файл `ej_deploy.pub` — это
ппубличный ключ, и файл `ej_deploy` — это приватный ключ. Публичный ключ
нужно добавить в список deploy keys в системе github.

#### Добавление deploy key в github

Для интеграции с github нужно сгенерированный публичный ключ добавить в
список deploy keys проекта на github.

Для добавления ключа на странице проекта перейдите в раздел "Settings".

[1](https://ejudge.ru/download/img/github-settings.png)

В разделе "Settings" выберите раздел "Deploy keys".

[2](https://ejudge.ru/download/img/github-settings-dk.png)

В разделе "Deploy keys" нажмите на "Add deploy keys".

[3](https://ejudge.ru/download/img/github-settings-dk-add.png)

В поле "Key" скопируйте <b>публичный</b> ключ, то есть содержимое файла
`ej_deploy.pub`.

Нажмите кнопку "Add Key".

#### Настройка задачи в ejudge

В задаче, для которой разрешена интеграция с github на странице с
условием задачи появится кнопка "Setup Version Control System
Integration".

[4](https://ejudge.ru/download/img/ejudge-setup-integration-button.png)

Если для данной задачи интеграция еще не была настроена, появится
диалоговое окно.

[5](https://ejudge.ru/download/img/ejudge-setup-integration-dialog.png)

При нажатии на кнопку "Ok" появится форма настройки интеграции.

[6](https://ejudge.ru/download/img/ejudge-setup-integration-form.png)

Поля "Git webhook" и "Git webhook token" заполняются автоматически и не
могут быть изменены. Значения этих полей потребуются при настройке
webhook в github.

В поле "Git type" нужно выбрать значение github.

В поле "Git SSH URL" нужно скопировать строку из поля URL вкладки Code
как показано ниже.

[7](https://ejudge.ru/download/img/github-clone-url.png)

В поле "Language" нужно вписать язык программирования, на котором
написано решение задачи.

В поле "Repo subdirectory" нужно вписать подкаталог репозитория, в
котором находится решение. Если решение находится непосредственно в
корне репозитория, оставьте это поле пустым.

Поле "Branch specification" оставьте пустым (в текущей версии выбор
отслеживаемой ветки репозитория не поддерживается).

В поле "SSH private key" скопируйте <b>приватный</b> ключ, то есть
содержимое файла `ej_deploy`.

[8](https://ejudge.ru/download/img/ejudge-setup-integration-form-filled.png)

После заполнения всех полей нажмите "Ok".

#### Настройка webhook в github репозитории

Для добавления Git webhook URL, сгенерированного при создании интеграции
в ejudge в проект github, нужно перейти в раздел "Settings" проекта
github.

В разделе "Settings" выберите раздел "Webhooks".

[9](https://ejudge.ru/download/img/github-settings-wh.png)

Нажмите на кнопку "Add webhook". После этого, возможно, потребуется еще
раз ввести пароль от github. Откроется форма настройки webhook.

[10](https://ejudge.ru/download/img/github-settings-wh-add.png)

В поле "Payload URL" скопируйте значение поля "Git webhook" из формы
настройки интеграции в ejudge, в поле "Content Type" выберите
"application/json", в поле "Secret" скопируйте значение поля "Get
webhook token" из формы настройки интеграции в ejudge. Остальные поля
можно оставить как есть.

После этого нажмите кнопку "Add webhook".

Настройка интеграции завершена. Если все шаги выполнены правильно, то
любой push в репозиторий будет приводить к отправке уведомления в
ejudge, после чего ejudge извлечет из репозитория последнюю версию,
выполнит ее компиляцию и тестирование.
