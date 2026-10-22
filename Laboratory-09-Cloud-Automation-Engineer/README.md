# Laboratory 09 — The Cloud Automation Engineer

## Mission Overview

This laboratory explores Linux automation using Bash scripting and Cron. A sample application directory is created, a script compresses the data into a timestamped backup archive, and a Cron job is configured to schedule the script every night at 2:00 AM.

## Objectives

- Understand Bash scripts, variables, and shebangs.
- Create and edit a script using Nano.
- Use `chmod +x` to grant execution permission.
- Compress application data into a `.tar.gz` archive.
- Configure a recurring Cron job.
- Document automation procedures in Markdown.
- Complete the ninth mission in the GitHub Cloud Computing Portfolio.

## Commands Executed

| Command | Purpose |
|---|---|
| `mkdir app-data` | Create the sample application directory |
| `echo "This is critical client data." > app-data/data.txt` | Create a test data file |
| `nano backup.sh` | Create and edit the Bash script |
| `chmod +x backup.sh` | Grant execution permission |
| `./backup.sh` | Run the backup script |
| `ls -l backups/` | List the generated backup archives |
| `tar -tzf backups/backup_*.tar.gz` | Inspect archive contents |
| `crontab -l` | List scheduled Cron jobs |
| `env EDITOR=nano crontab -e` | Edit the Cron schedule |

## Skills Learned

- Bash scripting and variable usage.
- Linux file and directory management.
- File permission configuration.
- Data compression using `tar`.
- Timestamped backup creation.
- Cron scheduling and task automation.
- Technical documentation and GitHub version control.

## Evidence

The `screenshots/` directory contains:

- `script-execution.png` — Evidence of successful script execution and backup creation.
- `cron-schedule.png` — Evidence of the installed Cron schedule.

## Conclusion

This mission demonstrates how recurring backup operations can be automated using Bash and Cron. Automating repetitive work can improve consistency and reduce manual effort, while verification and recovery testing remain necessary for dependable backups.
