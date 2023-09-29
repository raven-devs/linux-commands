# Timeout / intervan: cron

To schedule and automate the execution of tasks, scripts, or commands at specified intervals or on specific dates and times. These scheduled tasks are often referred to as "cron jobs.".

Cron jobs are defined and managed through "crontab" files, which are individual configuration files for each user. Each user can have their own set of scheduled tasks defined in their crontab file. System-wide tasks can also be scheduled by modifying the system's global crontab file or by placing scripts in specific directories, like `/etc/cron.daily` or `/etc/cron.hourly`.

Each line in a crontab file represents a scheduled task and has the following format:

```bash
* * * * * $command
```

- The five asterisks (\*) represent the time and date fields for scheduling the task, in order:

  1. Minute (0 - 59)
  2. Hour (0 - 23)
  3. Day of the month (1 - 31)
  4. Month (1 - 12 or "jan" - "dec")
  5. Day of the week (0 - 7 or "sun" - "sat"; both 0 and 7 represent Sunday)

## Usage

```bash
# run a script every day at 15:30 (3:30 PM)
30 15 * * * /path/to/script.sh

# schedule a task to run every Monday at 2:00 AM
0 2 * * 1 /path/to/script.sh

# run a script on the first day of each month at midnight
0 0 1 * * /path/to/script.sh

# run a script every 5 minutes (`*/5` in the first field represents "every 5 minutes.", it means that the command will run when the minute is divisible by 5, which equates to every 5 minutes)
*/5 * * * * /path/to/script.sh

# run a script every 3 hours (by specifying 0 in the first field, the job will run at the start of each hour; the second field specifies that the command should run when the hour is divisible by 3, which equates to every 3 hours)
0 */3 * * * /path/to/script.sh

# run a script every day (by specifying 0 in the first field, it means the job will run at the start of the hour; by specifying 0 in the second field, it means the job will run at midnight (00:00))
0 0 * * * /path/to/script.sh
```

## Crontab files

```bash
# edit your crontab file
crontab -e

# display your current crontab
crontab -l

# remove your current crontab
crontab -r
```

## Logging and Debugging

Cron jobs may produce output, which can be sent via email to the user who scheduled the task. To capture the output of a cron job, you can redirect it to a file

```bash
# This appends both standard output (stdout) and standard error (stderr) to the specified log file
* * * * * /path/to/script.sh >> /path/to/output.log 2>&1
```
