Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Интеграция
с github/gitlab](Интеграция_с_github/gitlab.md)/[Настройка
интеграции с gitlab для
пользователя](Настройка_интеграции_с_gitlab_для_пользователя.md)

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
нужно добавить в список deploy keys в системе gitlab.
