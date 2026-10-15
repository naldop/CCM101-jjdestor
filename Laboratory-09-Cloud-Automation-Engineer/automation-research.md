# Automation Research

## Bash Script
A Bash script is a plain text file containing a list of Linux commands that the
shell runs one after another, so you don't have to type them by hand each time.
The first line, `#!/bin/bash` (called the shebang), tells the system which
program should interpret the file. In this case, it says to use Bash.

## Variables
A variable stores a value under a name, like `BACKUP_DIR="backups"`, so the
script can reuse it anywhere by writing `$BACKUP_DIR`. Programmers use them so
that if the folder path changes, they only edit it in one place instead of
hunting through the whole script. It also reduces typos and makes the script
easier to read.

## Cron Job
A cron job is a task that Linux runs automatically on a schedule, such as every
night at 2:00 AM, using the cron service. It is essential for cloud operations
because servers need routine work like backups, log cleanup, and updates to
happen reliably without a human being awake to trigger them. It saves time and
keeps systems consistent across hundreds of machines.
