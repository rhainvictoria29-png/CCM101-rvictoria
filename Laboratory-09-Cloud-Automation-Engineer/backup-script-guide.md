# Backup Script Guide

## 1. Automated Backup Script

The following Bash script automates the backup of the `app-data` directory by compressing it into a `.tar.gz` archive. It also uses a timestamp to give each backup a unique filename.

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

## 2. Making the Script Executable

The command `chmod +x backup.sh` gives the script permission to execute.

Without this permission, attempting to run the script using `./backup.sh` may result in a "Permission denied" error.

After granting execute permission, the script can be run using:

```bash
./backup.sh
```

## 3. Cron Job Configuration

A Cron job allows a command or script to run automatically at a scheduled time.

The following Cron expression schedules the backup script to run every day at 2:00 AM:

```bash
0 2 * * * /root/backup.sh
```

## 4. Explanation of the Five Cron Fields

A Cron expression contains five time fields followed by the command to execute.

| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | Runs at minute zero |
| Hour | 2 | Runs at 2:00 AM |
| Day of Month | * | Runs on any day of the month |
| Month | * | Runs in any month |
| Day of Week | * | Runs on any day of the week |

The asterisk (`*`) means any or every possible value for that field.

Therefore, `0 2 * * * /root/backup.sh` means that the backup script is scheduled to execute every day at 2:00 AM.
