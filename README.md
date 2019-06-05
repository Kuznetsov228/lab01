## Laboratory work I

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Выполнить инструкцию учебного материала
- [x] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=Kuznetsov228 # Создать переменную окружения 
$ export GIST_TOKEN=<xxxxxxxxxxx> # Создать переменную окружения GIST_TOKEN
$ alias edit=vim # Теперь команда по вызову edit выполняется vim
```

```ShellSession
$ mkdir -p ${GITHUB_USERNAME}/workspace #Создание директории Kuznetsov228/workspace
$ cd ${GITHUB_USERNAME}/workspace #Смена директории
$ pwd #Полный путь
/home/kuza/Kuznetsov228/workspace
$ cd /home/sergeymarti/Kuznetsov228 #На уровень выше
$ pwd #Текущая директория
/home/kuza

```

```ShellSession
$ mkdir -p workspace/tasks/ #Создание папки
$ mkdir -p workspace/projects/ #Создание папки
$ mkdir -p workspace/reports/ #Создание папки
$ cd workspace #Переход в директорию workspace
```

```ShellSession
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz #Скачивание архива
$ tar -xf node-v6.11.5-linux-x64.tar.xz #Разархирование 
$ rm -rf node-v6.11.5-linux-x64.tar.xz #Удаление архива
$ mv node-v6.11.5-linux-x64 node #Переименовывание директории
```

```ShellSession
$ ls node/bin #Показать содержимое node/bin
# node  npm
$ echo ${PATH} #Вывести значение переменной PATH
#/home/kuza/bin:/usr/local/bin:/home/KuzaDrot/.local/bin:/usr/local/bin:/usr/bin:/cygdrive/c/Windows/system32:/cygdrive/c/Windows:/cygdrive/c/Windows/System32/Wbem:/cygdrive/c/Windows/System32/WindowsPowerShell/v1.0:/cygdrive/c/Program Files (x86)/NVIDIA Corporation/PhysX/Common:/cygdrive/c/Program Files/NVIDIA Corporation/NVIDIA NvDLISR:/cygdrive/c/Program Files/mingw-w64/x86_64-7.2.0-posix-seh-rt_v5-rev1/mingw64/bin

$ export PATH=${PATH}:`pwd`/node/bin #Запись нового значения в PATH
$ echo ${PATH} #Вывести значение PATH
#/home/kuza/bin:/usr/local/bin:/home/KuzaDrot/.local/bin:/usr/local/bin:/usr/bin:/cygdrive/c/Windows/system32:/cygdrive/c/Windows:/cygdrive/c/Windows/System32/Wbem:/cygdrive/c/Windows/System32/WindowsPowerShell/v1.0:/cygdrive/c/Program Files (x86)/NVIDIA Corporation/PhysX/Common:/cygdrive/c/Program Files/NVIDIA Corporation/NVIDIA NvDLISR:/cygdrive/c/Program Files/mingw-w64/x86_64-7.2.0-posix-seh-rt_v5-rev1/mingw64/bin:/home/KuzaDrot/node/bin

$ mkdir scripts #Создание папки scripts 
$ cat > scripts/activate<<EOF  #Запись строки в scripts
export PATH=\${PATH}:`pwd`/node/bin 
EOF
$ source scripts/activate #Запуск скрипта
```

```ShellSession
$ npm install -g gistup #Установка gistup
$ ls node/bin #Вывод содержимого bin
```

```ShellSession
$ cat > ~/.gistup.json <<EOF #Создаем файл .gistup.json, где будет находится наш gist token
{
  "token": "${GIST_TOKEN}"
}
EOF
```

## Report

```ShellSession
$ export LAB_NUMBER=01 # Добавляем переменную с номером л/р
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER} # Клонируем репозиторий с л/р в директорию tasks/lab01
$ mkdir reports/lab${LAB_NUMBER} # Создаем папку для хранения отчетов
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md # Копируем README.md в папку с отчетами и переименовываем его
$ cd reports/lab${LAB_NUMBER} # Переходим в папку с REPORT.md
$ edit REPORT.md # Редактируем его
$ gistup -m "lab${LAB_NUMBER}" # Создаем gist с сообщением 'lab01'
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
```$ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz #скачиваем архив```
2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0` 
``` $ tar -xf boost_1_69_0.tar.gz # распаковываем архив
$ rm -rf boost_1_69_0.tar.gz # удаляем архив
$ cd boost_1_69_0 # переходим в каталог с *boost*
```
3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории. ```#21 файлов ```
4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории. ```#61193 файлов ```
5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).
```
$ find . -type f -name '*.h' | wc -l
296
$ find . -type f -name '*.cpp' | wc -l
13774
$ find . -type f '!' -name '*.cpp' -a '!' -name '*.h' | wc -l
47121
```
6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*. $ find . -type f -name `any.hpp`
```'./boost/fusion/include/any.hpp
./boost/fusion/algorithm/query/any.hpp
./boost/fusion/algorithm/query/detail/any.hpp
./boost/spirit/home/support/algorithm/any.hpp
./boost/proto/detail/any.hpp
./boost/type_erasure/any.hpp
./boost/hana/fwd/any.hpp
./boost/hana/any.hpp
./boost/any.hpp
./boost/xpressive/detail/utility/any.hpp''''
```
7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
```$ grep -lr 'boost::asio' .
./boost/beast/experimental/core/impl/timeout_socket.hpp
...
./doc/html/process/reference.html
```
8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).
```$ ./bootstrap.sh --prefix=boost_output 
$ ./b2 install
```
9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
```$ cd ..
$ mv boost_1_69_0/boost_output boost-libs
```
10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
```$ du -h```
11. Найдите *топ10* самых "тяжёлых".
```$ find .  -type f -exec du -sh {} 2>/dev/null + | sort -rh | head -n 10
 27M	./lib/libboost_wave.a
 21M	./lib/libboost_log_setup.a
 19M	./lib/libboost_log.a
 16M	./lib/libboost_test_exec_monitor.a
 15M	./lib/libboost_unit_test_framework.a
9,2M	./lib/libboost_locale.a
8,7M	./lib/libboost_regex.a
8,2M	./lib/libboost_math_tr1f.a
7,9M	./lib/libboost_math_tr1.a
7,8M	./lib/libboost_math_tr1l.a


```
```
Copyright (c) 2015-2019 The ISC Authors
```
