Process management

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

File system

df -h -> to know all the mount points and space used by them
mkfs -> to format a disk
mount -> to mount a file system
umount -> to unmount a file system
ls -l  -> to list all the files and directories, shows information about file permissions and size 
tail -> display few last lines of a file
head -> display first few lines of a file
diff -> compares the content of two files line by line to show differences
chmod - change the permission of file/directory (read, write, execute)
chown - change the owner of a file/group
usermod - to modify existing user account 
useradd - to add a new user , use -m option to create a home directory
groupadd - to add a new group
groupown - to change the owner of a group
groupmod - to change the existing group 

Networking troubleshooting

ipaddr -> to know ip address 
ip a -> to know the ip address
ip route -> to check the default gateway

netstat / ss -> it provides information on active network connection, listening ports and routing table
netstat -tulnp - shows all TCP/UDP ports currently listening
nestat -a -> it shows all the active connections including both listening and non-listening ports
netstat -r -> shows kernel routing table, shows how your system redirects n/w traffic
netstat -i -> provides a summary of network interface, such as packets sent, recieved and error encountered
nestat -s -> shows detailed protocal info - TCP, UDP, ICPM, IP
nestat -c -> enables continious monitoring by refreshing the o/p every second.

curl -> to test the connectivity for http/https endpoints

curl -I http://google.com -> used to get the status code 

ping -> to test the connectivity from host to another host (ICMP protocol)
ping ip address/ ping hostname

nslookp/dig -> to resolve the hostname and check DNS record
nslookup google.com

traceroute -> traces the network path the packet takes to reach the destination
traceroute google.com

tcpdump -i etho -> 
tcpdump -nn host 192.168.1.50 and port 443 -> here -n reduces noisy DNS resolutions







ping -> to check if the server is responding
telnet ->
hostname ->
curl ->
nslookup ->

