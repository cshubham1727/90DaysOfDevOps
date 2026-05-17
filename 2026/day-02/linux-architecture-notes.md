Core Component of Linux:
Kernel: Kernel is main core component and it acts as primary interface between hardware and software components
Shell: It is Command Line Interface that acts as interface between user and kernel
User Space: It is a memory space where applications and background processes runs

How processes are created and managed
We can manage any new process in linux using 'Systemctl' command
systemctl start 'process name' -> to start a new process
systemctl stop 'process name' -> to stop a process
systemctl restart 'process name' -> to restart a process
systemctl status 'process name' -> to check the status of the process

Systemd
It is the first process which gets started when the system loads (boots the system) and its PID is 1
It manages other background processes (daemons) and user space processes using systemctl 

Different Process states
1. Running (R) : If the process is running
2. Interuptible Sleep (S) - The process is wating for a signal either from user or network response
3. Uninteruptible Sleep (D) - The process is wating for a I/O (disk access) and cannot be interupted by any signal unless the I/O completes.
4. Stopped (T) - If the process is terminated by user or any signal
5. Zombie (Z) - The process has finished its execution but still has entry in the process table so that its parent can read
6. its exit status. Once the parent 'reaps' this status using wait() system call, the process is removed completely.
'Reaping' a zombie process is a critical clean up step to collect the exit code from dead child processes, allowing the kernel
to remove the entry from process table using a command wait() or waitpid(), releasing the process ID for reuse.

5 Commands
1. Top -> to monitor real time usage of CPU and Memory, owner of process, PID
   While top command is running you can use below keys to modify the view
   k - to kill a process using PID
   M - Sort the processes by Memory usage
   P - Sort the processes by CPU usage
2. df -h -> display the disk usage by all the mounted file system
3. ps -> provides a snapshot of all the running processes
 ps aux -> to view all the procesess
 ps aux --sort=%mem = shows top memory consuming procesess
 ps aux --sort=%cpu = shows top CPU consuming procesess
 ps aux | grep [process name] = used to seach for a specific process
 ps -p [PID] = shows details of a process using PID
4. grep -> used to search specific string or pattern and print the output
   grep -e "error" -e "failed" log.txt -> -e is used to search multiple patterns at same time in a single file
   grep -r -> searches all files in the directory and sub-directories as well
   grep -n -> return each matching line with line no.
   grep -c -> total no. of lines that matches the pattern
   grep -i -> it searches case insensitive doesn't matter capital or small letters.
5. Find -> used to search files and directories in a real time within file structure based on user defines criteria
   filename, size, type, modification time
   . -> current directory search
   / -> root directory search

   find . -name "log.txt"
   find /var/log -type f - > It will list for all the files
   find /var/log -type d -> It will list all the directories
   find / -size +100M -> It will search all the files greater than 100 MB
   find . mtime -7 -> it will all the files modfied in last 7 days
   find .mmin 60 -> it will list all the files modified in last 60 mins
6. locate -> this command is also used to search files but in a pre existing DB and not in a real time like 'find' command does.

   






