`#!/bin/sh`  
`#`  
`# Подстановка для каталога, из которого будет загружаться файл foo.cfg`  
`LANG_CONFIG_DIR="@lang_config_dir@"`  
`#`  
`# Функция, выводящая параметры ЯП, не зависящие от его наличия в данной инсталляции`  
`function common_config()`  
`{`  
`  echo 'long_name="GNU Foo Interpreter"'`  
`  echo 'src_sfx=".foo"'`  
`  echo 'arch="linux-shared"'`  
`}`  
`#`  
`# Функция, генерирующая содержимое конфигурационного файла в случае ошибки`  
`# при конфигурировании ЯП foo`  
`function failure()`  
`{`  
`  # очищаем за собой временные файлы`  
`  rm -f conftest*`  
`  # генерируем пустую версию`  
`  echo 'version='`  
`  echo 'arg="'"${arg}"'"'`  
`  common_config`  
`  echo 'FOOPATH=/bin/false'`  
`  # в режиме -v довыводим "no"`  
`  [ "${verbose}" = 1 ] && echo "no" >&2`  
`  exit 1`  
`}`  
`#`  
`# Сбрасываем переменные окружения, отвечающие за языковое окружение`  
`# так как они могут влиять на вывод программ, который анализируется нашим скриптом`  
`unset LANG`  
`unset LC_ALL`  
`unset LC_MESSAGES`  
`unset LANGUAGE`  
`#`  
`# Если указана опция -v, включить флаг verbose`  
`if [ x"$1" = x-v ]`  
`then`  
`  verbose=1`  
`  shift`  
`fi`  
`if [ x"$1" = x-r ]`  
`then`  
`  #`  
`  # Режим конфигурирования ЯП (-r)`  
`  arg="$2"`  
`  # Если не задан явный путь к программе foo, устанавливаем его равным foo`  
`  # и расчитываем на то, что эта программа находится где-то в каталогах`  
`  # задаваемых переменной окружения PATH`  
`  [ x"$2" != x ] && foo="$2"`  
`  [ "${foo}" = "" ] && foo="foo"`  
`  # Дополнительный вывод в verbose-режиме`  
`  [ "${verbose}" = 1 ] && echo -n "checking whether GNU Foo Interpreter is available..." >&2`  
`  #`  
`  # Предварительный запуск программы foo. Проверяем, что она вообще запускается`  
`  # и поддерживает опцию --version`  
`  "${foo}" --version >/dev/null 2>&1 || failure`  
`  # Теперь выделяем номер версии из вывода программы`  
`  # Обратите внимание, что правила выделения номера версии зависят от формата вывода,`  
`  # который для разных ЯП не фиксирован, поэтому для нового ЯП здесь может`  
`  # находиться совершенно другая команда`  
``   version=`"${foo}" --version 2>&1 | gawk '{ print $2; }'` || failure ``  
`  # Если номер версии выделить не получилось, конфигурация неудачна`  
`  [ "${version}" != "" ] || failure`  
`  #`  
`  # Получаем полный путь к программе foo. Полный путь требуется в конструкции #!,`  
`  # которая помещается в начало программы`  
``   FOOPATH=`which "${foo}"` || failure ``  
`  [ "${FOOPATH}" != "" ] || failure`  
`  #`  
`  # Генерируем маленькую программку чтобы проверить работоспособность foo`  
`  echo "#! ${FOOPATH}" > conftest.foo`  
`  echo 'puts "OK"' >> conftest.foo`  
`  chmod +x ./conftest.foo || failure`  
`  #`  
`  # Запускаем ее и проверяем, что код завершения 0`  
`  ./conftest.foo >/dev/null 2>&1 || failure`  
`  #`  
`  # Удаляем рабочие файлы за собой`  
`  rm -f ./conftest*`  
`  # Генерируем содержимое конфигурационного файла`  
`  echo 'version="'"${version}"'"'`  
`  echo 'arg="'"${arg}"'"'`  
`  common_config`  
`  echo 'FOOPATH="'"${FOOPATH}"'"'`  
`  # Дополнительный вывод об успешности конфигурации`  
`  [ "${verbose}" = 1 ] && echo "yes, ${FOOPATH}, ${version}" >&2`  
`  exit 0`  
`fi`  
`#`  
`if [ x"$1" = x-l ]`  
`then`  
`  # Запуск в режиме листинга (-l)`  
`  echo "GNU Foo Interpreter `[`http://gnufoo.org`](http://gnufoo.org)`"`  
`  exit 0`  
`fi`  
`#`  
`# Поддерживаем переменную окружения EJUDGE_LANG_CONFIG, с помощью которой`  
`# можно явно задать путь к конфигурационному файлу ЯП`  
`[ "${EJUDGE_LANG_CONFIG}" = "" ] && EJUDGE_LANG_CONFIG="${LANG_CONFIG_DIR}/foo.cfg"`  
`#`  
`# Считываем конфигурационный файл ЯП, если он существует`  
`if [ -f "${EJUDGE_LANG_CONFIG}" ]`  
`then`  
`  . "${EJUDGE_LANG_CONFIG}"`  
`else`  
`  # Некоторый путь по умолчанию, если конфигурационный файл не существует`  
`  FOOPATH="/usr/bin/foo"`  
`fi`  
`#`  
`# Проверка, что ЯП поддерживается в данной инсталляции`  
`if [ x"${FOOPATH}" = x -o x"${FOOPATH}" = x/bin/false ]`  
`then`  
`  echo "This language is not supported." >&2`  
`  exit 1`  
`fi`  
`#`  
`if [ x"$1" = x-p ]`  
`then`  
`  # Режим печати пути к ЯП foo`  
`  echo "${FOOPATH}"`  
`  exit 0`  
`fi`  
`#`  
`# Проверяем, что foo запускается`  
`"${FOOPATH}" --version 2>/dev/null >/dev/null || exit 1`  
`#`  
`# Если требуется полный вывод (опция -f), начинаем печать`  
`[ x"$1" = x-f ] && echo -n "GNU Foo Interpreter "`  
`#`  
`# Извлекаем из вывода номер версии ЯП`  
`# См. комментарий выше`  
`"${FOOPATH}" --version 2>&1 | gawk '{ print $2; }'`
