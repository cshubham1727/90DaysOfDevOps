ps
    PID TTY          TIME CMD
   4175 pts/0    00:00:00 bash
   5744 pts/0    00:00:00 man
   5752 pts/0    00:00:00 pager
   7470 pts/0    00:00:00 ps

top
top -b -n 1 > top_output.txt

prep -u shubham -> it will list all the PID started by user shubham

systemctl status ssh -> show status as 'running'

systemctl list-units -> it list all the currently loaded and active systemd units in memory

journalctl -u ssh
journalctl -f ssh -> to view realtime logs of the service ssh

tail -n 20 filename
head -n 5 filename

both 'tail' and 'head' show 10 lines by default



