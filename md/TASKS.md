### [return main page](../README.md) || My Future Tasks :
* А можно сделать так чтобы кажый раз не переместиться в нужный файл использовать что то по быстрей и корочи путь? Например: Я нахожусь в директорий `gitlab/learn-technologies` и хочу сразу попасть в другую директорию, паример `github/learn-batch` А потом вернуться назат в Gitlab.

* În Bash File eu nu pot să scriu `title` așa cum în consolă obișnuită `cmd` și să scriu neme la fereastra din consolă. Și eu aș dori să fac așa ceva ca cînd scriu acest cuvînt în bash, să pot să pot schimba numele la geam. Mă refer la consolă, dacă ceva. :)

* Fă un script unde o să fie un folder cu 100 de fișiere `txt`. Dar înăuntru lor o să fie scris `Here is a simple document with number %number%`. Variabila `%number%` va arata numbărul cuvenit de la 1 - 100.

* Cum sa fac asa ca cuvintele cheie sa fie sortate dupa alfabet, adica chiar din fisier ?

* Теоретически я могу скачать сериалы, аниме или что то другое без того что бы каждый раз скачивать по одельности, каждый епизод.

* Cum să fac așa ceva: Am un fișier pustiu și vreau să înscriu ceva în el ? Spre Exemplu: Am lista de comenzi la node.js `node --help`. Ap eu vreu să înscriu într-un file aceste comenzi. Apoi, pasul doi, adica următor să traduc în limba rusă.

* Запуск команд от имени администратора :
```bat
@echo off
runas /user:Administrator "cmd.exe /c dir"
```

* Очистка временных файлов:
```bat
@echo off
del /s /q C:\Windows\Temp\*
```

* Создание резервной копии файлов :
```bat
@echo off
xcopy "C:\MyDocuments\*" "D:\Backup\" /s /e /h /y
```

* Перезагрузка компьютера :
```
@echo off
shutdown /r /f /t 0
```

* Пинг сервера или сайт а:
```bat
@echo off
ping google.com
```

* Переименование множества файлов :
```bat
@echo off
ren *.txt *.bak
```

* Запуск последовательности команд :
```bat
@echo off
cd C:\MyFolder
dir
pause
```

### Extern links :
* [ChatGPT - Примеры того что можно сделать с Bat Files](https://chatgpt.com/c/66fe1047-bd50-800f-9ca9-e28cf1e9cee5)
