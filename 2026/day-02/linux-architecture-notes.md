The core components of Linux (kernel, user space, init/systemd):

user space - The space where user writes the code 

Linux - The platform in which code is written or a bridge bw the user and the Hardware

kernel - it act as a barrier bw the user and the Hardware all the requests goes through Kernel then to hardware and hardware also respond back to kernel then to user.
handles: System and process management
         Networking 
         Security
         

user - User_space(Linux) - kernel - Hardware


SYStemd - It the first process runs after boot 
Handles : ssh 
          nginx 
          Docker



Linux Process States

Running (R)
Process is currently executing on the CPU.
Example: A script or application actively working.

Sleeping (S)
Process is waiting for an event (input, network response, file access).
Most processes spend their time in this state.
Example: Web server waiting for a request.

Uninterruptible Sleep (D)
Waiting for I/O operations (disk, hardware).
Cannot be interrupted until the operation finishes.
Example: Reading data from a disk.

Stopped (T)
Process execution is paused.
Usually stopped manually or by a debugger.
Example:
Ctrl + Z

Zombie (Z)
Process has finished execution, but its parent has not collected its exit status.
Consumes very little memory but indicates poor process management.
Example: Child process terminated but parent process didn't clean it up.


5 Linux Commands I Use Daily
1. ps
View running processes.

Example:

ps aux
2. top
Real-time system and process monitoring.

Example:

top
3. grep
Search for specific text or patterns.

Example:

grep "error" app.log
4. df -h
Check disk space usage.

Example:

df -h
5. tail -f
Monitor logs in real time.

Example:

tail -f /var/log/syslog
Quick DevOps Use Case
Check running services: ps aux
Monitor server health: top
Search errors in logs: grep
Verify disk space: df -h
Watch application logs: tail -f

These commands are used almost daily by Linux administrators and DevOps engineers for troubleshooting and monitoring.
