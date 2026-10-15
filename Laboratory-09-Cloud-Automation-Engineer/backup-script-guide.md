# Backup Script Guide

This guide documents the automated backup script created for CloudNova
Technologies so the client's IT team can understand how it works.

## 1. The Full Script (backup.sh)

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## 2. What the `chmod +x` Command Does

By default, Linux treats a new text file as plain data, not a program, so
trying to run it gives a "Permission denied" error. The command
`chmod +x backup.sh` changes the file's permissions to add the **execute**
(`x`) permission. After that, the system allows the file to be run as a
program with `./backup.sh`.

## 3. The Cron Expression

The expression used is:

```
0 2 * * * /root/backup.sh
```

| Field | Value | Meaning |
|-------|-------|---------|
| Minute | `0` | At minute 0 (the top of the hour) |
| Hour | `2` | At 2 AM (24-hour clock) |
| Day of Month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |

Together, this schedules the backup to run **every night at exactly 2:00 AM**.
