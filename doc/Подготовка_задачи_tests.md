Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Виды
задач](Виды_задач "wikilink")/[Задача на написание
тестов](Задача:tests "wikilink")/[Подготовка
задачи](Подготовка_задачи_tests "wikilink")

Задачи этого типа являются самыми сложными для подготовки. При описании
подготовки таких задач будет предполагаться, что турнир настраивается в
[альтернативной раскладке
файлов](Альтернативная_раскладка_файлов "wikilink"), то есть все файлы,
относящиеся к задаче, размещаются в одном каталоге.

### Настройка основных параметров задачи

Поскольку задача на написание тестов предполагает запуск программ на
тестовых данных аналогично стандартной задаче, в разделе конфигурации
задачи должны быть установлены параметры, относящиеся к тестированию
задач. Например:

`# Идентификационные параметры задачи`  
[`id`](Serve.cfg:problem:id "wikilink")` = ...`  
[`short_name`](Serve.cfg:problem:short_name "wikilink")` = ...`  
[`long_name`](Serve.cfg:problem:long_name "wikilink")` = ...`  
`# Основные параметры задачи`  
[`test_sfx`](Serve.cfg:problem:test_sfx "wikilink")` = ".dat"            # Суффикс имен файлов с тестовыми данными`  
[`use_corr`](Serve.cfg:problem:use_corr "wikilink")`                     # Проверка использует файлы с правильными ответами`  
[`corr_dir`](Serve.cfg:problem:corr_dir "wikilink")` = "`[`%Ps`](Форматная_подстановка "wikilink")`"             # Каталог с файлами с правильными ответами - значение не важно`  
[`corr_sfx`](Serve.cfg:problem:corr_sfx "wikilink")` = ".ans"            # Суффикс имен файлов с правильным ответом`  
[`use_stdin`](Serve.cfg:problem:use_stdin "wikilink")`                    # Программа считывает результат со стандартного потока ввода`  
[`use_stdout`](Serve.cfg:problem:use_stdout "wikilink")`                   # Программа выводит результат на стандартный поток вывода`  
[`standard_checker`](Serve.cfg:problem:standard_checker "wikilink")` = "`[`cmp_int`](cmp_int "wikilink")`" # Проверка - сравнение двух целых чисел`  
[`time_limit`](Serve.cfg:problem:time_limit "wikilink")` = 1               # Ограничение времени ЦП - 1 секунда`  
[`real_time_limit`](Serve.cfg:problem:real_time_limit "wikilink")` = 5          # Ограничение реального времени - 5 секунд`  
[`max_stack_size`](Serve.cfg:problem:max_stack_size "wikilink")` = 8M          # Ограничение размера стека - 8 мегабайт`  
[`max_vm_size`](Serve.cfg:problem:max_vm_size "wikilink")` = 64M            # Ограничение общего размера вирт. памяти - 64 мегабайта`

Идентификационные параметры задачи — это идентификатор задачи
[`id`](Serve.cfg:problem:id "wikilink"), короткое название
[`short_name`](Serve.cfg:problem:short_name "wikilink"), полное название
[`long_name`](Serve.cfg:problem:long_name "wikilink") и, возможно,
внутреннее название задачи
[`internal_name`](Serve.cfg:problem:internal_name "wikilink").

Значение параметра [`corr_dir`](Serve.cfg:problem:corr_dir "wikilink")
несущественно, так как предполагается что турнир настраивается в
альтернативной раскладке файлов. Тем не менее, параметр `corr_dir`
должен быть установлен в некоторое непустое значение.

### Настройка дополнительных параметров для задач на разработку тестов

Для задачи на написание тестов должны быть установлены следующие
параметры задачи.

[`type`](Serve.cfg:problem:type "wikilink")` = "`[`tests`](Задача:tests "wikilink")`"`  
[`binary`](Serve.cfg:problem:binary "wikilink")  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/x-gzip"`  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/x-compress"`  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/x-bzip2"`  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/x-tar"`  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/zip"`

Параметр [`type`](Serve.cfg:problem:type "wikilink") задает тип задачи
как задачу на разработку тестов. Параметр
[`binary`](Serve.cfg:problem:binary "wikilink") разрешает прием двоичных
файлов в качестве решений. Параметр
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")
разрешает прием архивных файлов в качестве решений.

### Настройка проверки правильности сдаваемого архива

Архив, сдаваемый участником на проверку, должен быть проверен на
корректность. Необходимо проверить, что файлы в архиве по отдельности и
все в целом удовлетворяют ограничениям на размер и количество файлов,
что имена всех файлов заданы корректно, что в архиве отсутствуют лишние
файлы. Эта проверка должна быть выполнена без разархивирования архива в
файловую систему во избежание потенциальных дыр в безопасности. Такая
проверка выполняется программой
[style_archive](style_archive "wikilink"), поставляемой в составе
ejudge.

Чтобы включить проверку сдаваемых архивов необходимо добавить в раздел
описания задачи определение конфигурационной переменной
[`style_checker_cmd`](Serve.cfg:problem:style_checker_cmd "wikilink").

[`style_checker_cmd`](Serve.cfg:problem:style_checker_cmd "wikilink")` = "`[`@prefix@`](Подстановка_параметров_configure "wikilink")`/libexec/ejudge/checkers/style_archive"`

Здесь `@prefix@` будет автоматически заменен на каталог, в который
проинсталлирована система ejudge. Параметры проверки архива на
целостность программе [style_archive](style_archive "wikilink") можно
передавать либо с помощью командной строки, либо с помощью переменных
окружения. В разделе конфигурации задачи можно воспользоваться
механизмом передачи параметров с помощью переменных окружения.

Чтобы включить режим проверки тестов необходимо задать переменную
окружения `EJ_TESTS_MODE`.

[`style_checker_env`](Serve.cfg:problem:style_checker_env "wikilink")` = "EJ_TESTS_MODE=1"`

Чтобы установить максимальный размер файла в архиве равным 1 килобайт
необходимо задать переменную окружения `EJ_MAX_FILE_SIZE`.

[`style_checker_env`](Serve.cfg:problem:style_checker_env "wikilink")` = "EJ_MAX_FILE_SIZE=1K"`

Чтобы установить максимальное количество тестов (то есть пар файлов c
входными данными и с правильным ответом) равным 10 необходимо задать
переменую окружения `EJ_MAX_TEST_COUNT`.

[`style_checker_env`](Serve.cfg:problem:style_checker_env "wikilink")` = "EJ_MAX_TEST_COUNT=10"`

Параметр `style_checker_env` может повторяться в разделе описания задачи
несколько раз. Для полного описания поддерживаемых программой
[style_archive](style_archive "wikilink") переменных окружения смотрите
[ее описание](style_archive "wikilink").

### Настройка проверки тестов

Файлы с тестовыми данными, сданные на проверку, должны быть
предварительно проверены на корректность [проверяющей программой для
тестов](Test_checkers "wikilink"). Провеяющая программа для тестов
должна проверить входной и выходной форматы файлов, ограничения на
входные данные. Кроме того, программа может проверить соответствие
входных данных и ответа.

Имя проверяющей программы для тестов задается с помощью конфигурационной
переменной
[`test_checker_cmd`](Serve.cfg:problem:test_checker_cmd "wikilink"). При
необходимости дополнительные переменные окружения могут задаваться с
помощью конфигурационной переменной
[`test_checker_env`](Serve.cfg:problem:test_checker_env "wikilink").

[`test_checker_cmd`](Serve.cfg:problem:test_checker_cmd "wikilink")` = "testcheck"`

В этом примере имя проверяющей программы — `testcheck`.

### Итоговая конфигурация задачи

С учетом всего вышесказанного, раздел конфигурации задачи может
выглядеть следующим образом.

[`id`](Serve.cfg:problem:id "wikilink")` = ...`  
[`short_name`](Serve.cfg:problem:short_name "wikilink")` = ...`  
[`long_name`](Serve.cfg:problem:long_name "wikilink")` = ...`  
[`type`](Serve.cfg:problem:type "wikilink")` = "`[`tests`](Задача:tests "wikilink")`"`  
[`test_sfx`](Serve.cfg:problem:test_sfx "wikilink")` = ".dat"`  
[`use_corr`](Serve.cfg:problem:use_corr "wikilink")  
[`corr_dir`](Serve.cfg:problem:corr_dir "wikilink")` = "`[`%Ps`](Форматная_подстановка "wikilink")`"`  
[`corr_sfx`](Serve.cfg:problem:corr_sfx "wikilink")` = ".ans"`  
[`use_stdin`](Serve.cfg:problem:use_stdin "wikilink")  
[`use_stdout`](Serve.cfg:problem:use_stdout "wikilink")  
[`standard_checker`](Serve.cfg:problem:standard_checker "wikilink")` = "`[`cmp_int`](cmp_int "wikilink")`"`  
[`time_limit`](Serve.cfg:problem:time_limit "wikilink")` = 1`  
[`real_time_limit`](Serve.cfg:problem:real_time_limit "wikilink")` = 5`  
[`max_stack_size`](Serve.cfg:problem:max_stack_size "wikilink")` = 8M`  
[`max_vm_size`](Serve.cfg:problem:max_vm_size "wikilink")` = 64M`  
[`binary`](Serve.cfg:problem:binary "wikilink")  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/x-gzip"`  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/x-compress"`  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/x-bzip2"`  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/x-tar"`  
[`enable_language`](Serve.cfg:problem:enable_language "wikilink")` = "application/zip"`  
[`style_checker_cmd`](Serve.cfg:problem:style_checker_cmd "wikilink")` = "`[`@prefix@`](Подстановка_параметров_configure "wikilink")`/libexec/ejudge/checkers/style_archive"`  
[`style_checker_env`](Serve.cfg:problem:style_checker_env "wikilink")` = "EJ_TESTS_MODE=1"`  
[`style_checker_env`](Serve.cfg:problem:style_checker_env "wikilink")` = "EJ_MAX_FILE_SIZE=1K"`  
[`style_checker_env`](Serve.cfg:problem:style_checker_env "wikilink")` = "EJ_MAX_TEST_COUNT=10"`  
[`test_checker_cmd`](Serve.cfg:problem:test_checker_cmd "wikilink")` = "testcheck"`

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
[libchecker](libchecker "wikilink").

`#include "`[`checkutils.h`](Libchecker:Заголовочные_файлы "wikilink")`"`  
  
`#include <limits.h>`  
  
`int`  
`main(int argc, char **argv)`  
`{`  
`  int x, y, z;`  
  
`  /* проверить, что передано правильное число аргументов командной строки */ `  
`  if (argc != 3) `[`fatal_CF`](libchecker:fatal_CF "wikilink")`("wrong number of arguments");`  
  
`  /* открыть файл с тестовыми данными и прочитать два числа */`  
`  `[`checker_in_open`](libchecker:checker_SRC_open "wikilink")`(argv[1]);`  
`  `[`checker_read_int_ex`](libchecker:checker_read_TYPE_ex "wikilink")`(`[`f_arr`](libchecker:Глобальные_переменные "wikilink")`[0], `[`fatal_PE`](libchecker:fatal_PE "wikilink")`, "x", 1, &x);`  
`  `[`checker_read_int_ex`](libchecker:checker_read_TYPE_ex "wikilink")`(`[`f_arr[0`](libchecker:Глобальные_переменные "wikilink")`], `[`fatal_PE`](libchecker:fatal_PE "wikilink")`, "y", 1, &y);`  
`  `[`checker_eof`](libchecker:checker_eof "wikilink")`(`[`f_arr[0`](libchecker:Глобальные_переменные "wikilink")`], `[`fatal_PE`](libchecker:fatal_PE "wikilink")`, "test input");`  
`  `[`checker_in_close`](libchecker:checker_SRC_close "wikilink")`();`  
  
`  /* проверить ограничения на входные данные */`  
`  if (x < SHRT_MIN || x > SHRT_MAX)`  
`    `[`fatal_PE`](libchecker:fatal_PE "wikilink")`("first value is out of range");`  
`  if (y < SHRT_MIN || y > SHRT_MAX)`  
`    `[`fatal_PE`](libchecker:fatal_PE "wikilink")`("second value is out of range");`  
  
`  /* открыть файл с правильным ответом и прочитать число */ `  
`  `[`checker_out_open`](libchecker:checker_SRC_open "wikilink")`(argv[2]);`  
`  `[`checker_read_int_ex`](libchecker:checker_read_TYPE_ex "wikilink")`(`[`f_arr[1`](libchecker:Глобальные_переменные "wikilink")`], `[`fatal_PE`](libchecker:fatal_PE "wikilink")`, "z", 1, &z);`  
`  `[`checker_eof`](libchecker:checker_eof "wikilink")`(`[`f_arr[1`](libchecker:Глобальные_переменные "wikilink")`], `[`fatal_PE`](libchecker:fatal_PE "wikilink")`, "test answer");`  
`  `[`checker_out_close`](libchecker:checker_SRC_close "wikilink")`();`  
  
`  /* проверить правильность ответа */ `  
`  if (z != x + y)`  
`    `[`fatal_WA`](libchecker:fatal_WA "wikilink")`("wrong answer");`  
  
`  return 0;`  
`}`

Эту программу назовем `testcheck.c` и поместим в каталог с файлами
задачи. Обратите внимание, что [внутренняя ошибка
проверки](внутренняя_ошибка_проверки "wikilink") выдается в случае
неправильного использования самой программы проверки тестов. Если
входной файл или файл правильного ответа не соответствуют ограничениям
задачи, выдается [ошибка неправильного формата
результата](ошибка_неправильного_формата_результата "wikilink").

Если в файле правильного ответа на самом деле записан неправильный
ответ, программа проверки тестов выдает ошибку [неправильный
ответ](неправильный_ответ "wikilink"). Это не обязательно. Неправильные
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
