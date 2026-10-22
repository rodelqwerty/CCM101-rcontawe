
# Checkpoint 6 — Technical Documentation
## Automated Backup Script Guide

### 1. Overview

This document explains the automated backup process created for the CloudNova Technologies laboratory. The Bash script compresses the `app-data` directory into a timestamped `.tar.gz` archive and saves it in the `backups` directory. A Cron job can schedule the script to run automatically every day at 2:00 AM, reducing the need for manual backups.

### 2. Complete Backup Script

The following is the complete code for `backup.sh`:

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p "$BACKUP_DIR"

# Compress the source directory into a timestamped archive
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully at $TIMESTAMP!"
```

### 3. Explanation of the Script

- **`#!/bin/bash`** — Specifies Bash as the interpreter used to execute the script.
- **`SOURCE_DIR="app-data"`** — Defines the directory containing the application data to back up.
- **`BACKUP_DIR="backups"`** — Defines the directory where backup archives are stored.
- **`TIMESTAMP=$(date +"%Y%m%d_%H%M%S")`** — Generates a timestamp for the backup filename, using the year, month, day, hour, minute, and second.
- **`mkdir -p "$BACKUP_DIR"`** — Creates the backup directory if it does not already exist.
- **`tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"`** — Compresses the source directory into a `.tar.gz` archive with a unique timestamped filename.
- **`echo`** — Displays messages indicating that the backup process has started and completed.

### 4. File Permissions

**Command executed:**

```bash
chmod +x backup.sh
```

The `chmod +x` command adds execute permission to `backup.sh`, allowing the file to be run as a program. After applying this permission, the script can be executed using:

```bash
./backup.sh
```

This command should be run from the directory containing `backup.sh`. If the script is stored elsewhere, use its correct path.

### 5. Manual Execution and Verification

Run the backup script:

```bash
./backup.sh
```

List the generated backup archives:

```bash
ls -lh backups/
```

The backup directory should contain timestamped `.tar.gz` files when the script runs successfully and the `app-data` directory exists.

To inspect the contents of a backup archive, use:

```bash
tar -tzf backups/backup_YYYYMMDD_HHMMSS.tar.gz
```

Replace `YYYYMMDD_HHMMSS` with the timestamp from an actual backup filename.

### 6. Cron Job Configuration

Cron is a Linux scheduling utility that automatically executes commands at specified times.

**Cron expression used:**

```cron
0 2 * * * /root/backup.sh
```

This expression schedules `/root/backup.sh` to run every day at 2:00 AM according to the server's configured timezone.

#### Breakdown of the Five Cron Time Fields

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | Runs at minute zero. |
| Hour | `2` | Runs at 2 AM. |
| Day of Month | `*` | Runs every day of the month. |
| Month | `*` | Runs every month. |
| Day of Week | `*` | Runs every day of the week. |

**How to read the expression:**

`0 2 * * *` means minute `0`, hour `2`, every day of the month, every month, and every day of the week.

#### Configure the Cron Job

Open the root user's crontab:

```bash
crontab -e
```

Add this line:

```cron
0 2 * * * /root/backup.sh
```

Save the file and exit the editor.

Verify the scheduled job:

```bash
crontab -l
```

The output should include:

```cron
0 2 * * * /root/backup.sh
```

**Note:** The cron expression above is the required configuration. The initial `crontab -l` output showed only default comments, so the job must be added and verified before it can run automatically.

### 7. Conclusion

This checkpoint documented the Bash backup script, the purpose of executable file permissions, and the configuration of a daily Cron schedule. The script creates timestamped compressed archives of the application data, while Cron automates its execution at 2:00 AM each day. Regularly verifying backup files and testing restoration helps ensure that important application data can be recovered when needed.
