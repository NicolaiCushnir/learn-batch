
### Double click :
1. Adaugă new task `tutorial_online_run_server_auto`
2. La task scrie asta : `/dir "D:\Documents\Develop\Gitlab\tutorial-online"`
3. Pur șl simplu înainte de `cd` apasă enter, să fie din rînd nou.
4. {bash::bash} cd /d D:\Documents\Develop\Gitlab\tutorial-online && nodemon tutorial_online.js
5. Deja the script `server_run.cmd` :

```bash
@echo off
cd /d "%~dp0"

start "" "D:\Programs\cmder\vendor\conemu-maximus5\ConEmu64.exe" -run {tutorial_online_run_server_auto}
```

### Addition
* cmder/settings/tasks ...
