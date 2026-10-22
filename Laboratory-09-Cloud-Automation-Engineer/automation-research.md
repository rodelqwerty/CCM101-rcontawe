
# Automation Research

## 1. Bash Script

A Bash script is a text file containing Linux commands that can be executed together to automate a task. The `#!/bin/bash` line at the beginning is called a shebang, and it tells the operating system which interpreter should run the script.

## 2. Variables

Variables store values such as folder paths, filenames, and timestamps so they can be reused throughout a script. For example, `$BACKUP_DIR` lets a programmer change the backup location in one place instead of repeatedly typing the full path.

## 3. Cron Job

A cron job is a scheduled task managed by the Linux Cron service. It is useful in cloud operations because recurring work, such as backups and maintenance, can run automatically at specified times without someone manually entering commands.

## 4. Purpose of This Mission

This mission demonstrates how Bash scripting and Cron can automate the backup of application data. The script creates a timestamped compressed archive, while the Cron scheduler is configured to run the script every day at 2:00 AM.
