### [return main page](../README.md) | Examples :

Имя и расширение текущего bat-файла, без пути
```bat
@echo off
echo %~nx0
```

Simple for loop
```bat
@echo off
for %%a in (one two three) do echo %%a
```

Записавыет в файл
```bat
@echo off
chcp 1251
help > "HELP_COMMAND.txt"
```

Dacă ai nevoie de ajutor de la un cuvînt cheie din `bat-file` atunci scrie în fișieul tău, de exemplu : `main.bat`, Scrie help și cuvîntrul de care ai nevoie. Exemple : `help path`, `help diruse`, `dnscmd`, `DOSKEY`. Full list is [here](https://ss64.com/nt/)
```bat
help dir
```

Не знаю что эта за фигня `/A` но поддерживает арифметические операции.
```bat
SET /A four=2+2
```

* Show curent date and time.

```bat
@echo off

rem Wa1 1
echo %date%, %time%

rem Way 2
for /F "tokens=2" %%i in ('date /t') do set mydate=%%i
set mytime=%time%
echo Current time is : %mydate%:%mytime%
```

* **Important !** Am automatizat file : `nodemon main.js` 

```bat
@echo off
cd ../Documents/Developer/Github/my-projects/node-server
%AppData%\npm\nodemon.cmd main.js
```

* O să deschidă automat în programa cmder 4 console
```bat
@echo off
start "" "%cmder_root%\Cmder.exe" /START %CD%
start "" "%cmder_root%\Cmder.exe" /START %CD%
start "" "%cmder_root%\Cmder.exe" /START %CD%
start "" "%cmder_root%\Cmder.exe" /START %CD%
exit
```
