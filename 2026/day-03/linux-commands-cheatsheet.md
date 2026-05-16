1. Process management

top -> to view real time CPU/Memory usage of process 
M -> to sort by memory usage
P -> to sort by CPU usage
htop -> helps to scroll through processes

ps aux > to list all the active processes
ps -> to list all the procesess
pgrep docker -> it will list all docker related procesess with PID
pidof bash -> it will provide pid of bash

kill PID -> it will termniate that process of given PID
kill -9 PID -> it will kill that process forcefully
pkill -u username - > it will kill all the processes owned by that specific user
killall node -> it will kill all the processes of node.js  

uptime -> provides how long the system has been running and provides current load average (1 , 5, 15 mins)

nohup ./script.sh  -> runs a script in a background that won't stop even if SSH connection is termininated

jobs -> list all the terminated and background procesess with job IDs
fg -> move the process to foreground so that user can interact with it
fg %1 -> It will bring the JobID#1 back to forground so that you can interact with it
bg -> move the process to background
bg %1 -> it will move the JobID#1 to background

systemctl -> to start, stop, restart, and know status of services
journalctl -> to manage logs
journalctl -f -> to view the logs in realtime similar to tail -f
journalctl -u apache -> to view logs of specific unit
journalctl -p err -> It will filter the logs with 'err'
journalct -g "[keyword]" -> to search using keyword
journalctl --since "2026-02-05 07:00:00" --until "2026-02-06 13:00:00" 

lsof -> list all files and processes that opened them
lsof -i :8080 -> finds all the processes listening on port 8080

nice -n 10 ./backup.sh -> it will move the backup job to priority 10
renice -n 5 -p 123

2. File system


df -h -> to know all the mount points and space used by them
mkfs -> to format a disk
mount -> to mount a file system
umount -> to unmount a file system


Networking troubleshooting
ipaddr -> to know ip address 
ping -> to check if the server is responding
telnet ->
hostname ->
curl ->
nslookup ->

