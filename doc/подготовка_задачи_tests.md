Навигация: [Главная страница](main_Page.md)/[Система
ejudge](система_ejudge.md)/[Использование](использование.md)/[Виды
задач](виды_задач.md)/[Задача на написание
тестов](задача/tests.md)/[Подготовка
задачи](подготовка_задачи_tests.md)

Задачи этого типа являются самыми сложными для подготовки. При описании
подготовки таких задач будет предполагаться, что турнир настраивается в
[альтернативной раскладке
файлов](альтернативная_раскладка_файлов.md), то есть все файлы,
относящиеся к задаче, размещаются в одном каталоге.

### Настройка основных параметров задачи

Поскольку задача на написание тестов предполагает запуск программ на
тестовых данных аналогично стандартной задаче, в разделе конфигурации
задачи должны быть установлены параметры, относящиеся к тестированию
задач. Например:

`# Идентификационные параметры задачи`  
[`id`](serve.cfg/problem/id.md)` = ...`  
[`short_name`](serve.cfg/problem/short_name.md)` = ...`  
[`long_name`](serve.cfg/problem/long_name.md)` = ...`  
`# Основные параметры задачи`  
[`test_sfx`](serve.cfg/problem/test_sfx.md)` = ".dat"            # Суффикс имен файлов с тестовыми данными`  
[`use_corr`](serve.cfg/problem/use_corr.md)`                     # Проверка использует файлы с правильными ответами`  
[`corr_dir`](serve.cfg/problem/corr_dir.md)` = "`[`%Ps`](Форматная_подстановка.md)`"             # Каталог с файлами с правильными ответами - значение не важно`  
[`corr_sfx`](serve.cfg/problem/corr_sfx.md)` = ".ans"            # Суффикс имен файлов с правильным ответом`  
[`use_stdin`](serve.cfg/problem/use_stdin.md)`                    # Программа считывает результат со стандартного потока ввода`  
[`use_stdout`](serve.cfg/problem/use_stdout.md)`                   # Программа выводит результат на стандартный поток вывода`  
[`standard_checker`](serve.cfg/problem/standard_checker.md)` = "`[`cmp_int`](cmp_int.md)`" # Проверка - сравнение двух целых чисел`  
[`time_limit`](serve.cfg/problem/time_limit.md)` = 1               # Ограничение времени ЦП - 1 секунда`  
[`real_time_limit`](serve.cfg/problem/real_time_limit.md)` = 5          # Ограничение реального времени - 5 секунд`  
[`max_stack_size`](serve.cfg/problem/max_stack_size.md)` = 8M          # Ограничение размера стека - 8 мегабайт`  
[`max_vm_size`](serve.cfg/problem/max_vm_size.md)` = 64M            # Ограничение общего размера вирт. памяти - 64 мегабайта`

Идентификационные параметры задачи — это идентификатор задачи
[`id`](serve.cfg/problem/id.md), короткое название
[`short_name`](serve.cfg/problem/short_name.md), полное название
[`long_name`](serve.cfg/problem/long_name.md) и, возможно,
внутреннее название задачи
[`internal_name`](serve.cfg/problem/internal_name.md).

Значение параметра [`corr_dir`](serve.cfg/problem/corr_dir.md)
несущественно, так как предполагается что турнир настраивается в
альтернативной раскладке файлов. Тем не менее, параметр `corr_dir`
должен быть установлен в некоторое непустое значение.

### Настройка дополнительных параметров для задач на разработку тестов

Для задачи на написание тестов должны быть установлены следующие
параметры задачи.

[`type`](serve.cfg/problem/type.md)` = "`[`tests`](задача/tests.md)`"`  
[`binary`](serve.cfg/problem/binary.md)  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/x-gzip"`  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/x-compress"`  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/x-bzip2"`  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/x-tar"`  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/zip"`

Параметр [`type`](serve.cfg/problem/type.md) задает тип задачи
как задачу на разработку тестов. Параметр
[`binary`](serve.cfg/problem/binary.md) разрешает прием двоичных
файлов в качестве решений. Параметр
[`enable_language`](serve.cfg/problem/enable_language.md)
разрешает прием архивных файлов в качестве решений.

### Настройка проверки правильности сдаваемого архива

Архив, сдаваемый участником на проверку, должен быть проверен на
корректность. Необходимо проверить, что файлы в архиве по отдельности и
все в целом удовлетворяют ограничениям на размер и количество файлов,
что имена всех файлов заданы корректно, что в архиве отсутствуют лишние
файлы. Эта проверка должна быть выполнена без разархивирования архива в
файловую систему во избежание потенциальных дыр в безопасности. Такая
проверка выполняется программой
[style_archive](style_archive.md), поставляемой в составе
ejudge.

Чтобы включить проверку сдаваемых архивов необходимо добавить в раздел
описания задачи определение конфигурационной переменной
[`style_checker_cmd`](serve.cfg/problem/style_checker_cmd.md).

[`style_checker_cmd`](serve.cfg/problem/style_checker_cmd.md)` = "`[`@prefix@`](подстановка_параметров_configure.md)`/libexec/ejudge/checkers/style_archive"`

Здесь `@prefix@` будет автоматически заменен на каталог, в который
проинсталлирована система ejudge. Параметры проверки архива на
целостность программе [style_archive](style_archive.md) можно
передавать либо с помощью командной строки, либо с помощью переменных
окружения. В разделе конфигурации задачи можно воспользоваться
механизмом передачи параметров с помощью переменных окружения.

Чтобы включить режим проверки тестов необходимо задать переменную
окружения `EJ_TESTS_MODE`.

[`style_checker_env`](serve.cfg/problem/style_checker_env.md)` = "EJ_TESTS_MODE=1"`

Чтобы установить максимальный размер файла в архиве равным 1 килобайт
необходимо задать переменную окружения `EJ_MAX_FILE_SIZE`.

[`style_checker_env`](serve.cfg/problem/style_checker_env.md)` = "EJ_MAX_FILE_SIZE=1K"`

Чтобы установить максимальное количество тестов (то есть пар файлов c
входными данными и с правильным ответом) равным 10 необходимо задать
переменую окружения `EJ_MAX_TEST_COUNT`.

[`style_checker_env`](serve.cfg/problem/style_checker_env.md)` = "EJ_MAX_TEST_COUNT=10"`

Параметр `style_checker_env` может повторяться в разделе описания задачи
несколько раз. Для полного описания поддерживаемых программой
[style_archive](style_archive.md) переменных окружения смотрите
[ее описание](style_archive.md).

### Настройка проверки тестов

Файлы с тестовыми данными, сданные на проверку, должны быть
предварительно проверены на корректность [проверяющей программой для
тестов](test_checkers.md). Провеяющая программа для тестов
должна проверить входной и выходной форматы файлов, ограничения на
входные данные. Кроме того, программа может проверить соответствие
входных данных и ответа.

Имя проверяющей программы для тестов задается с помощью конфигурационной
переменной
[`test_checker_cmd`](serve.cfg/problem/test_checker_cmd.md). При
необходимости дополнительные переменные окружения могут задаваться с
помощью конфигурационной переменной
[`test_checker_env`](serve.cfg/problem/test_checker_env.md).

[`test_checker_cmd`](serve.cfg/problem/test_checker_cmd.md)` = "testcheck"`

В этом примере имя проверяющей программы — `testcheck`.

### Итоговая конфигурация задачи

С учетом всего вышесказанного, раздел конфигурации задачи может
выглядеть следующим образом.

[`id`](serve.cfg/problem/id.md)` = ...`  
[`short_name`](serve.cfg/problem/short_name.md)` = ...`  
[`long_name`](serve.cfg/problem/long_name.md)` = ...`  
[`type`](serve.cfg/problem/type.md)` = "`[`tests`](задача/tests.md)`"`  
[`test_sfx`](serve.cfg/problem/test_sfx.md)` = ".dat"`  
[`use_corr`](serve.cfg/problem/use_corr.md)  
[`corr_dir`](serve.cfg/problem/corr_dir.md)` = "`[`%Ps`](Форматная_подстановка.md)`"`  
[`corr_sfx`](serve.cfg/problem/corr_sfx.md)` = ".ans"`  
[`use_stdin`](serve.cfg/problem/use_stdin.md)  
[`use_stdout`](serve.cfg/problem/use_stdout.md)  
[`standard_checker`](serve.cfg/problem/standard_checker.md)` = "`[`cmp_int`](cmp_int.md)`"`  
[`time_limit`](serve.cfg/problem/time_limit.md)` = 1`  
[`real_time_limit`](serve.cfg/problem/real_time_limit.md)` = 5`  
[`max_stack_size`](serve.cfg/problem/max_stack_size.md)` = 8M`  
[`max_vm_size`](serve.cfg/problem/max_vm_size.md)` = 64M`  
[`binary`](serve.cfg/problem/binary.md)  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/x-gzip"`  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/x-compress"`  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/x-bzip2"`  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/x-tar"`  
[`enable_language`](serve.cfg/problem/enable_language.md)` = "application/zip"`  
[`style_checker_cmd`](serve.cfg/problem/style_checker_cmd.md)` = "`[`@prefix@`](подстановка_параметров_configure.md)`/libexec/ejudge/checkers/style_archive"`  
[`style_checker_env`](serve.cfg/problem/style_checker_env.md)` = "EJ_TESTS_MODE=1"`  
[`style_checker_env`](serve.cfg/problem/style_checker_env.md)` = "EJ_MAX_FILE_SIZE=1K"`  
[`style_checker_env`](serve.cfg/problem/style_checker_env.md)` = "EJ_MAX_TEST_COUNT=10"`  
[`test_checker_cmd`](serve.cfg/problem/test_checker_cmd.md)` = "testcheck"`

Часть этих параметров можно перенести в раздел абстрактной задачи.

### Написание проверяющей программы для тестов

Следующий шаг — написание программы для проверки корректности тестов.
Эта программа получает два аргумента командной строки: имя файла с
тестовыми данными и имя файла с правильным результатом работы. Программа
проверки корректности тестов может, в принципе, модифицировать и первый,
и второй файл. Для последующего тестирования будут передаваться уже
модифицированные файлы.

Рассмотрим программу для проверки корректности тестов для задачи
сложения двух целых чисел. На стандартном потоке ввода задаются два
целых числа в диапазоне \[-32768;32767\]. На стандартный поток вывода
необходимо напечатать сумму этих чисел.

Программу проверки корректности тестов можно писать на любом языке (в
том числе и скриптовом). В нашем случае эта программа будет написана на
языке Си с использованием библиотеки
[libchecker](libchecker.md).

`#include "`[`checkutils.h`](libchecker/Заголовочные_файлы.md)`"`  
  
`#include <limits.h>`  
  
`int`  
`main(int argc, char **argv)`  
`{`  
`  int x, y, z;`  
  
`  /* проверить, что передано правильное число аргументов командной строки */ `  
`  if (argc != 3) `[`fatal_CF`](libchecker/fatal_CF.md)`("wrong number of arguments");`  
  
`  /* открыть файл с тестовыми данными и прочитать два числа */`  
`  `[`checker_in_open`](libchecker/checker_SRC_open.md)`(argv[1]);`  
`  `[`checker_read_int_ex`](libchecker/checker_read_TYPE_ex.md)`(`[`f_arr`](libchecker/Глобальные_переменные.md)`[0], `[`fatal_PE`](libchecker/fatal_PE.md)`, "x", 1, &x);`  
`  `[`checker_read_int_ex`](libchecker/checker_read_TYPE_ex.md)`(`[`f_arr[0`](libchecker/Глобальные_переменные.md)`], `[`fatal_PE`](libchecker/fatal_PE.md)`, "y", 1, &y);`  
`  `[`checker_eof`](libchecker/checker_eof.md)`(`[`f_arr[0`](libchecker/Глобальные_переменные.md)`], `[`fatal_PE`](libchecker/fatal_PE.md)`, "test input");`  
`  `[`checker_in_close`](libchecker/checker_SRC_close.md)`();`  
  
`  /* проверить ограничения на входные данные */`  
`  if (x < SHRT_MIN || x > SHRT_MAX)`  
`    `[`fatal_PE`](libchecker/fatal_PE.md)`("first value is out of range");`  
`  if (y < SHRT_MIN || y > SHRT_MAX)`  
`    `[`fatal_PE`](libchecker/fatal_PE.md)`("second value is out of range");`  
  
`  /* открыть файл с правильным ответом и прочитать число */ `  
`  `[`checker_out_open`](libchecker/checker_SRC_open.md)`(argv[2]);`  
`  `[`checker_read_int_ex`](libchecker/checker_read_TYPE_ex.md)`(`[`f_arr[1`](libchecker/Глобальные_переменные.md)`], `[`fatal_PE`](libchecker/fatal_PE.md)`, "z", 1, &z);`  
`  `[`checker_eof`](libchecker/checker_eof.md)`(`[`f_arr[1`](libchecker/Глобальные_переменные.md)`], `[`fatal_PE`](libchecker/fatal_PE.md)`, "test answer");`  
`  `[`checker_out_close`](libchecker/checker_SRC_close.md)`();`  
  
`  /* проверить правильность ответа */ `  
`  if (z != x + y)`  
`    `[`fatal_WA`](libchecker/fatal_WA.md)`("wrong answer");`  
  
`  return 0;`  
`}`

Эту программу назовем `testcheck.c` и поместим в каталог с файлами
задачи. Обратите внимание, что [внутренняя ошибка
проверки](внутренняя_ошибка_проверки.md) выдается в случае
неправильного использования самой программы проверки тестов. Если
входной файл или файл правильного ответа не соответствуют ограничениям
задачи, выдается [ошибка неправильного формата
результата](ошибка_неправильного_формата_результата.md).

Если в файле правильного ответа на самом деле записан неправильный
ответ, программа проверки тестов выдает ошибку [неправильный
ответ](неправильный_ответ.md). Это не обязательно. Неправильные
ответы можно и не выявлять на стадии проверки тестов, тогда на стадии
запуска тестовых программ корректные программы не пройдут эти тесты, что
тоже будет диагностировано как ошибка в тестах, предъявленных на
проверку.

### Подготовка тестовых программ

При работе турнира в альтернативной раскладке файлов тесты к задачам
размещаются в каталоге tests каталога задачи. В случае задачи на
написание тестов в каталоге tests должны находиться два каталога:
`good`, в который помещаются программы, правильно решающие задачу,
которые должны проходить все тесты, и `fail`, в который помещаются
программы, содержащие ошибку, которые не должны проходить все тесты.

Каталоги `good` и `fail` могут иметь произвольную структуру. Для запуска
на выполнение при проверке тестов будут выбираться только регулярные
файлы, размещенные непосредственно в этих каталогах (то есть рекурсивный
обход подкаталогов не выполняется). Из регулярных файлов выбираются
только файлы, у которых установлен бит выполнения `x`. Все прочие файлы
игнорируются. Таким образом, в этих каталогах могут находится исходные
тексты программ `.c`, `.cpp` и прочие файлы, при условии, что у исходных
текстов программ не установлен бит `x`.

Файлы, запускаемые на выполнение, могут быть произвольными файлами,
исполнение которых поддерживается в данной операционной системе,
например, бинарными исполняемымы файлами, скриптами на языках perl,
python и т. д. Система ejudge не поддерживает автоматическую компиляцию
файлов, аналогичную автоматической компиляции проверяющих программ, но
поддерживается запуск make в каталоге задачи, с помощью которого можно
компилировать и тестовые программы.

Обратите внимание, что тестовые программы запускаются в обычном
(незащищенном) режиме, поэтому рекомендуется аудит тестовых программ с
целью предотвращения потенциальных нарушений безопасности.

### Написание Makefile

Для перекомпиляции программы проверки тестов, проверяющей программы и
тестовых программ необходимо написать `Makefile`. Этот файл должен
располагаться в каталоге задачи (там где располагаются исходники
программы проверки тестов и каталог `tests`). Система ejudge вызывает
программу make каждый раз, когда выполняется операция "Check contests
settings".

Файл `Makefile` может быть примерно таким:

`# Переменная окружения EJUDGE_PREFIX_DIR передается в make при выполнении Check contests settings автоматически`  
`# но если ее нет (например, make вызывается из командной строки), то установим вручную`  
`ifndef EJUDGE_PREFIX_DIR`  
`EJUDGE_PREFIX_DIR = /opt/ejudge`  
`endif`  
  
`# Установка опций компилятора gcc для использования libchecker`  
`EJUDGE_CONFIG = ${EJUDGE_PREFIX_DIR}/bin/ejudge-config`  
`LIBCHECKER_CFLAGS = $(shell ${EJUDGE_CONFIG} --cflags)`  
`LIBCHECKER_LDFLAGS = $(shell ${EJUDGE_CONFIG} --ldflags)`  
`LIBCHECKER_LIBS = $(shell ${EJUDGE_CONFIG} --libs)`  
  
`CC = gcc`  
`CFLAGS = -Wall -Werror -O2 -std=gnu99 -Wno-pointer-sign ${LIBCHECKER_CFLAGS} ${LIBCHECKER_LDFLAGS}`  
`LD = gcc`  
`LDLIBS = ${LIBCHECKER_LIBS}`  
  
`# Берем все файлы, которые необходимо скомпилировать`  
`GOOD_CFILES = $(wildcard tests/good/*.c)`  
`GOOD_XFILES = $(GOOD_CFILES:.c=)`  
  
`FAIL_CFILES = $(wildcard tests/fail/*.c)`  
`FAIL_XFILES = $(FAIL_CFILES:.c=)`  
  
`all : ejudge_make_problem`  
  
`# При запуске из ejudge утилита make вызывается с целью ejudge_make_problems`  
`ejudge_make_problem : testcheck ${GOOD_XFILES} ${FAIL_XFILES}`  
  
`clean:`  
`        -rm -f testcheck ${GOOD_XFILES} ${FAIL_XFILES}`
