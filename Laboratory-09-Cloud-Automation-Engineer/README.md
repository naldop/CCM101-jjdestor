# Laboratory 09: Cloud Automation Engineer

## Mission Overview
In this lab, I took the role of a Cloud Automation Engineer for CloudNova
Technologies. My mission was to write a Bash script that automatically backs
up client data, make it executable, and schedule it to run every night using
a cron job.

## Objectives
- Research the basics of Bash scripts, variables, and cron jobs
- Write a Bash script that compresses client data into a timestamped backup
- Grant execution permissions to the script using chmod
- Schedule the script to run automatically at 2:00 AM using cron
- Document the work for the client's IT team

## Commands Executed
- `mkdir app-data` and `echo "..." > app-data/data.txt`: created dummy client data
- `nano backup.sh`: wrote the backup script
- `chmod +x backup.sh`: made the script executable
- `./backup.sh`: ran the script
- `ls -l backups/`: verified the backup file
- `crontab -l`: viewed scheduled jobs
- `env EDITOR=nano crontab -e`: edited the cron table
- `git add`, `git commit`, `git push`: saved work to GitHub

## Skills Learned
- Writing and running Bash scripts
- Using variables and timestamps in scripts
- Managing Linux file permissions with chmod
- Compressing files with tar
- Scheduling recurring tasks with cron
- Writing clear technical documentation
