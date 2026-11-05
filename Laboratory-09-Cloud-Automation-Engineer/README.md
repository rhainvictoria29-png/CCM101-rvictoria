# Laboratory 09 – The Cloud Automation Engineer

## 1. Mission Overview

This laboratory activity focuses on cloud automation using Bash scripting and Cron jobs in an Ubuntu environment. The mission is to create an automated backup script that compresses a sample application data directory into a `.tar.gz` archive and schedules the backup to run automatically every day at 2:00 AM.

## 2. Objectives

- Understand the role of Bash scripting in cloud automation.
- Create a sample application data directory.
- Develop a Bash script that automatically backs up and compresses files.
- Apply executable permissions to a Bash script using `chmod +x`.
- Configure a Cron job to schedule automatic backups.
- Document the commands, script, and scheduling configuration.

## 3. Commands Executed

The following commands were used during the laboratory activity:

| Command | Purpose |
|---|---|
| `mkdir app-data` | Creates the application data directory. |
| `echo "This is critical client data." > app-data/data.txt` | Creates a sample data file. |
| `cat app-data/data.txt` | Displays the contents of the sample file. |
| `nano backup.sh` | Creates and edits the Bash backup script. |
| `cat backup.sh` | Displays the script contents. |
| `./backup.sh` | Attempts to execute the backup script. |
| `chmod +x backup.sh` | Grants executable permission to the script. |
| `ls -l backup.sh` | Checks the script's file permissions. |
| `ls -l backups/` | Displays the generated backup archive. |
| `crontab -l` | Displays the current Cron schedule. |
| `env EDITOR=nano crontab -e` | Opens the Cron configuration in Nano for editing. |

The Cron expression configured was:

```bash
0 2 * * * /root/backup.sh
```

This schedules the backup script to execute every day at 2:00 AM.

## 4. Skills Learned

Through this activity, I learned how to create and execute a Bash automation script, manage file permissions, compress application data into backup archives, and configure Cron jobs for scheduled tasks. I also gained practical experience using Linux terminal commands and understanding how automation helps simplify repetitive system administration tasks.
