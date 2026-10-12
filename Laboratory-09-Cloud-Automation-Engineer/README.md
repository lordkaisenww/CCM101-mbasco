# Laboratory 9: The Cloud Automation Engineer

## Mission Overview
[your words: 2-3 sentences. What was the problem the client had, and what did you build to solve it?]

## Objectives
- Understand the fundamental syntax of a Bash shell script, including variables and basic commands.
- Use a command-line text editor (nano) to write and save executable scripts.
- Modify Linux file permissions using the chmod command.
- Understand task scheduling and the syntax of a Linux crontab.
- Document automation code and Cron job configurations using Markdown.
- Complete the final chapter of the GitHub Cloud Computing Portfolio.

## Commands Executed

| Command | Purpose |
|---|---|
| `mkdir app-data` | Created a dummy folder to represent the client's data |
| `echo "This is critical client data." > app-data/data.txt` | Created a test file inside the folder |
| `nano backup.sh` | Opened the nano editor to write the backup script |
| `./backup.sh` | Ran the script (first attempt failed with "Permission denied") |
| `chmod +x backup.sh` | Made the script executable |
| `ls -l backups/` | Verified the compressed backup file was created |
| `crontab -l` | Listed the current cron jobs |
| `env EDITOR=nano crontab -e` | Opened the crontab in nano to add the schedule |

## Skills Learned
- [your words: bullet about Bash scripting]
- [your words: bullet about file permissions]
- [your words: bullet about cron scheduling]
- [your words: bullet about documentation or troubleshooting, such as the typo and path issues you hit]

## Screenshots
- `screenshots/script-execution.png`
- `screenshots/cron-schedule.png`
