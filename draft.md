ps ax
/PROC/[PID_number]/
```
cmdline - содержит команду с помощью которой был запущен процесс, а также переданные ей параметры
cwd - символическая ссылка на текущую рабочую директорию процесса
exe - ссылка на исполняемый файл
root - ссылка на папку суперпользователя
environ - переменные окружения, доступные для процесса
fd - содержит файловые дескрипторы, файлы и устройства, которые использует процесс
maps, statm, и mem - информация о памяти процесса
stat, status - состояние процесса
```
advanced  
/PROC/DISKSTATS - Статистика ввода и вывода на блочные устройства  
/PROC/LOADAVG - load average  
/PROC/UPTIME

interest  
/PROC/KCORE - слепок памяти  
PROC/SYSRQ-TRIGGER - общение с ядром

#### рабочие наброски   
```
ll /proc/[$PID]/exe|awk '{print $11}' - выведет бинарник для $PID  
grep State /proc/[$PID]/status|awk '{print $2" "$3}'   # выведет состояние процесса
```