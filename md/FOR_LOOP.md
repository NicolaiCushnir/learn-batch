### [return main page](../README.md) | For Loop

for loop without iteration. 
```bat
@echo off
ECHO Here is file for_loop.bat
SET count=1
FOR /f "tokens=*" %%G IN ('DIR /b') DO (
	ECHO %count%:%%G
	SET /a count+=1)
```

for loop with a iteration. And this script count number at your bat files.
```bat
@echo off
SET count=1
FOR /f "tokens=*" %%G IN ('dir /b') DO (call :subroutine "%%G")
GOTO :eof

:subroutine
 echo %count%:%1
 set /a count+=1
 GOTO :eof
```

### Explication
Нумерованные элементы для чтения из каждой строки или для string to process

### Links:
* [intro in For Loop](https://ss64.com/nt/for.html)