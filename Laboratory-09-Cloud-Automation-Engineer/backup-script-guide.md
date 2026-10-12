
cat > backup-script-guide.md << 'EOF'
# Backup Script Guide

This guide documents the automated backup solution built for CloudNova Technologies so the client's IT team can understand, maintain, and reuse it.

## 1. The Backup Script (`backup.sh`)

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

**What the script does:** The script sets the source folder, backup folder, and current date and time. It creates the backup folder if it does not exist and compresses the app-data folder into a .tar.gz file. After the backup is created, it displays a message showing that the backup is completed.

## 2. What `chmod +x` Did

```bash
chmod +x backup.sh
```

The chmod +x command gives the script permission to execute. Before using this command, Linux showed "Permission denied" because the file did not have execute permission. After adding the permission, I was able to run the script using ./backup.sh.

## 3. The Cron Expression

```
0 2 * * * /root/backup.sh
```

| Field | Value | Allowed Range | Meaning in this job |
|---|---|---|---|
| Minute | `0` | 0-59 | Runs at minute 0 |
| Hour | `2` | 0-23 | Runs at 2 AM |
| Day of Month | `*` | 1-31 | Runs every day |
| Month | `*` | 1-12 | Runs every month |
| Day of Week | `*` | 0-7 (0 and 7 = Sunday) | Runs every day of the week |

**Overall meaning:** The cron job automatically runs the backup script every day at 2:00 AM based on the server's time.

## 4. Verification

- Ran `./backup.sh` manually and confirmed a `.tar.gz` file appeared in `backups/` (see `screenshots/script-execution.png`).
- Confirmed the cron job is installed with `crontab -l` (see `screenshots/cron-schedule.png`).
EOF
