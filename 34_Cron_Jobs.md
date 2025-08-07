
# 📝 Linux Commands Analysis Notes

This document contains detailed notes on the commands executed and their observed effects, based on the terminal session.

---

## 📌 `pwd` — Print Working Directory

### ➤ Command:
```bash
pwd
```
### ➤ Output:
```
/home/omkar
```
### ➤ Description:
Displays the full absolute path of the current working directory.

---

## 📌 `ls` — List Directory Contents

### ➤ Command:
```bash
ls
```
### ➤ Output (initial):
Shows a list of files and folders in `/home/omkar`, like:
```
'a b c.mp4'  cpTest  file1.txt  merged.txt  ...
```
### ➤ Description:
Used to list all files and directories in the current location.

---

## 📌 `crontab -e` — Edit Crontab File

### ➤ Command:
```bash
crontab -e
```
### ➤ Output:
```
no crontab for omkar - using an empty one
Select an editor...
```
### ➤ Description:
Opens the user's cron table to schedule tasks. If it's the first time, asks to select an editor.

#### ➤ Example:
If you choose option `1` (nano), it will create a new crontab file and open it in nano.

---

## 📌 `cat` — View File Content

### ➤ Command:
```bash
cat hello.log
```
### ➤ Output:
```
hello
hello
hello
hello
Good Evening
```
### ➤ Description:
Used to read the content of files.

#### ➤ Example:
If the file `hello.log` is being written to by a cron job or manually, running `cat` will show its updated contents.

---

## 📌 `date` — Show System Date and Time

### ➤ Command:
```bash
date
```
### ➤ Output:
```
Thu Aug  7 17:07:32 IST 2025
```
### ➤ Description:
Displays the current system date and time.

---

## 🧠 Observations from the Session

- After setting up the cron job using `crontab -e`, the file `hello.log` started getting updated repeatedly with `hello`, indicating a repeating cron job was running.
- Later, manual input like `Good Evening` appeared, suggesting manual editing or another job/script wrote to `hello.log`.

---

## ✅ Summary of Commands Used

| Command       | Purpose                                 |
|---------------|------------------------------------------|
| `pwd`         | Show current directory path              |
| `ls`          | List files and directories               |
| `crontab -e`  | Edit the cron job list for the user      |
| `cat`         | View contents of a file                  |
| `date`        | Show current date and time               |

---

## 💡 Tips

- Use `crontab -l` to **view current cron jobs**.
- Use `crontab -r` to **remove your cron table**.
- Make sure your script has execute permissions if you're using it in a cron job.
omkar@LAPTOP-4UCI9HKV:~$ crontab -l
# Edit this file to introduce tasks to be run by cron.
#
# Each task to run has to be defined through a single line
# indicating with different fields when the task will be run
# and what command to run for the task
#
# To define the time you can provide concrete values for
# minute (m), hour (h), day of month (dom), month (mon),
# and day of week (dow) or use '*' in these fields (for 'any').
#
# Notice that tasks will be started based on the cron's system
# daemon's notion of time and timezones.
#
# Output of the crontab jobs (including errors) is sent through
# email to the user the crontab file belongs to (unless redirected).
#
# For example, you can run a backup of all your user accounts
# at 5 a.m every week with:
# 0 5 * * 1 tar -zcf /var/backups/home.tgz /home/
#
# For more information see the manual pages of crontab(5) and cron(8)
#
# m h  dom mon dow   command

11 17 * * * echo "Good Evening" >> ~/hello.log

