Day 4 – Linux Processes & Service Management

1. Process Checks

Commands Used
ps aux
ps -ef
top

What I Observed
Viewed running processes and their PIDs.
Checked CPU and memory utilization.
Identified parent and child processes.

Learning
Every running application in Linux is a process.
PID (Process ID) uniquely identifies a process.
top provides real-time system monitoring.


2. Service Checks

Commands Used
systemctl status ssh
systemctl status cron
systemctl list-units --type=service

What I Observed
Verified service status.
Checked whether services were active, inactive, or failed.

Learning
systemctl is used to manage services under systemd.
Services can be started, stopped, restarted, and enabled.



3. Log Checks

Commands Used:
journalctl -xe
journalctl -u ssh
tail -f /var/log/syslog

What I Observed:
Viewed service-related logs.
Identified timestamps and error messages.
Monitored logs in real time.

Learning:
Logs help diagnose issues and understand system behavior.
journalctl is the primary tool for viewing systemd logs.


4. Mini Troubleshooting Exercise
Scenario

SSH service not responding.

Steps Followed
systemctl status ssh : Checked service status.

journalctl -u ssh : Reviewed logs for errors.

sudo systemctl restart ssh : Restarted the service.

systemctl status ssh : Verified that the service was running successfully.



Troubleshooting Flow

Issue Reported
      ↓
Check Service Status
      ↓
Review Logs
      ↓
Apply Fix
      ↓
Restart Service
      ↓
Verify Resolution



Key Takeaways

Learned how to inspect running processes.
Practiced checking and managing systemd services.
Used logs for troubleshooting.
Followed a basic production-style troubleshooting workflow.

