### [return main page](../README.md) | Topic 3. Variables
Самый Простой способ объявить переменную - написать :
```bat
@echo off
set text=Here is a simple text for me.
echo %text%
```

**Note 1** Обезательно исользуете обычный `cmd`, тоесть команду строку. `WIN + R cmd`.

**Note 2** Не используйте пробелы между именем переменой и иё значением; `set text = Here is a simple text for me.` не будет работать, но `set text=Here is a simple text for me.` Это уже заработает.

**Note 3** `%var_word%` используеться в обычном режиме консолю, а `%%var_word%%` когда мы работаем внутри файла, например `main.js`. А еще я хочу обратить ваше внимание на то что когда мы пишем `%var_word`, это параметр.

**Note 4** Буть отсорожен! Ключевое слово `SET` может удалить динамические переменые таких как `%DATE%` или `%CD%`.  Вы можете перечислить эти динамические переменные, просмотрев конец текста справки для SET, вызываемого вызовом `SET /?` в вашем `bat` файле.

**Question** What is this ? : `SETLOCAL`, `ENDLOCAL`, `EXIT`. 

**What ?** Переменная `%~dp0`. Переменная %~dp0 (это ноль) при ссылке на нее в пакетном файле Windows заменяется на букву диска и путь к этому пакетному файлу. Переменные %0-%9 относятся к параметрам командной строки пакетного файла.

**Что делает pushd %~ dp0 ?**
Сохраните текущий каталог в стеке и измените на % ~ dp0, который является диском и путем «0-го» параметра командной строки (который является самой командой), поэтому путь назначения, который нужно установить, — это диск/ путь к пакетному файлу для выполнения.07 сентября 2017 г.

### Local and Global variable
По умолчанию переменные являются глобальными для всего сеанса командной строки. Вызовите `SETLOCAL` 

```bat
@echo off

:: SETGLOBAL
SET var_1=var_1 Global vaiable

SETLOCAL
SET var_2=var_2 Local Variable

ECHO %var_1%
ECHO %var_2%
ENDLOCAL
```

Теперь давайте посмотрим, что происходит, когда мы пытаемся использовать локальную переменную за пределами ее области видимости, т.е. используя after `ENDLOCAL`.

```bat
@echo off

:: SETGLOBAL
SET var_1=var_1 Global vaiable

SETLOCAL
SET var_2=var_2 Local Variable

ECHO %var_1%

ENDLOCAL
:: Aici sa terminat local variable with name : var_2
:: Și anume a ajutat ENDLOCAL.

ECHO %var_2%
```

Итак, как видно из этого вывода, когда мы пытаемся использовать локальную переменную за пределами ее области, вместо выполнения команд с локальной переменной `ECHO` отключается.

### What is with these variables ?
* %USERPROFILE% - Write in `fille.cmd`
* %COMPSPEC%
* %date% - Write in `fille.cmd`
* %time% - Write in `fille.cmd`
