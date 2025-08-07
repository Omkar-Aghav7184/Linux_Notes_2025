* * * * * command to be executed

1.Minute(0-59)
2.Hour(0-23)
3.Day of Month (1-31)
4.Month (1-12)
5.Day of Week (0-6 where 0 is for Sunday and 6 is for Saturday)

Asterisk(*): Matches any value for the respective time Unit.
Comma(,): Specifies a list of values.
Hyphen(-): Specifies a range of values.
Slash(/): Specifies a step value for the range.
For example: */5 in the minute field means every 5 minutes 

*     *     *     *     *     command
│     │     │     │     │
│     │     │     │     └───── Day of week (0 - 7) (Sunday is 0 or 7)
│     │     │     └────────── Month (1 - 12)
│     │     └─────────────── Day of month (1 - 31)
│     └──────────────────── Hour (0 - 23)
└───────────────────────── Minute (0 - 59)


---

## ✅ Common Examples

| Cron Expression       | Description                              |
|-----------------------|------------------------------------------|
| `0 0 * * *`           | Every day at midnight                    |
| `0 9 * * *`           | Every day at 9:00 AM                     |
| `*/5 * * * *`         | Every 5 minutes                          |
| `0 */2 * * *`         | Every 2 hours                            |
| `30 14 * * 1-5`       | Weekdays (Mon–Fri) at 2:30 PM            |
| `0 10 1 * *`          | On the 1st of every month at 10:00 AM    |
| `0 0 1 1 *`           | Every year on Jan 1st at midnight        |
| `0 22 * * 1-5`        | Mon–Fri at 10:00 PM                      |
| `0 6,18 * * *`        | Every day at 6:00 AM and 6:00 PM         |

---

## 🧪 Example with Command

Run a backup script every day at 1:00 AM:

```bash
0 1 * * * /home/omkar/scripts/backup.sh

Special Strings (Shorthand)
Shortcut	Equivalent	Description
@reboot	—	Run at system startup
@daily	0 0 * * *	Every day at midnight
@weekly	0 0 * * 0	Every Sunday at 12 AM
@monthly	0 0 1 * *	First day of month
@yearly	0 0 1 1 *	First day of the year

Use crontab -e to edit your crontab and add jobs.
crontab -l     # List your current cron jobs
crontab -e     # Edit cron jobs

