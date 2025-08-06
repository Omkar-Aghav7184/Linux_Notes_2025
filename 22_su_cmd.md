# 🧾 Linux Command Analysis Notes

This file contains notes on **correct** and **incorrect** Linux commands used in your session, along with their proper usage and explanations.

---

## ✅ Correct Commands

### `ls`
Lists files and directories in the current working directory.
```bash
ls
whoami
Shows the current logged-in user.

bash
Always show details

Copy
whoami
pwd
Prints the current working directory.

bash
Always show details

Copy
pwd
cd ..
Moves up one directory level.

bash
Always show details

Copy
cd ..
cut -d: -f1 /etc/passwd
Displays the list of all user accounts.

bash
Always show details

Copy
cut -d: -f1 /etc/passwd
cut -d: -f1,7 /etc/passwd
Displays all usernames and their login shells.

bash
Always show details

Copy
cut -d: -f1,7 /etc/passwd
sudo passwd redis
Changes the password for the redis user (requires sudo privileges).

bash
Always show details

Copy
sudo passwd redis
sudo passwd root
Changes the password for the root user.

bash
Always show details

Copy
sudo passwd root
su --login root or su - root
Switches to the root user using a login shell.

bash
Always show details

Copy
su --login root
# or
su - root
su - omkar
Switches to user omkar (after being root).

bash
Always show details

Copy
su - omkar
❌ Incorrect Commands and Fixes
pw
❌ Incorrect: pw is not a valid command.
✅ Correct: To print working directory use:

bash
Always show details

Copy
pwd
su -root
❌ Incorrect: This is parsed as option -r to su, which is invalid.
✅ Correct:

bash
Always show details

Copy
su - root
su passwd root
❌ Incorrect: You're trying to switch to a non-existent user called passwd.
✅ Correct to change password:

bash
Always show details

Copy
sudo passwd root
su -om
❌ Incorrect: -om is interpreted as options. There's no such option.
✅ Correct: If om is the username (which it isn't in your case):

bash
Always show details

Copy
su - om
⚠️ Special Notes
Users like redis and www-data have shells like /usr/sbin/nologin and cannot log in normally.

To allow login for such users, you must change their shell:

bash
Always show details

Copy
sudo chsh -s /bin/bash redis
✅ End of Notes
"""