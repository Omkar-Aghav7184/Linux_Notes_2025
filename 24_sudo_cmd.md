# 🔐 Linux User & Directory Permission Commands - Analysis & Notes

This document explains each command executed in the session, step-by-step, including mistakes and corrections.

---

## 📂 1. List Files in Current Directory

```bash
ls
Lists files/folders in the current directory

2. Print Current Working Directory
pwd
Shows full path of current directory.


🔙 3. Move to Parent Directory
cd ..
Moves one level up in the directory tree.


📁 4. Navigate to Home and Root Directories
cd /home
cd /
Navigates to /home and then root /.


🚫 5. Create Directory in Root (without sudo)
mkdir meals
❌ Incorrect if you're not root or don't have sudo rights.

Error: Permission denied

✅ Correct Usage:
sudo mkdir meals

📃 6. List All Files in Root with Details
ls -l
Displays permissions, owners, sizes, and dates.

✅ Correct usage.

👤 7. Switch User
su - ooo
Switches to user ooo with a login shell.

Prompts for ooo's password.

✅ Correct usage.

🔒 8. Try Sudo as Non-Sudo User
sudo ls
❌ Incorrect for non-sudo users

Error: ooo is not in the sudoers file.

✅ Fix:
Either:

Log in as a sudo-enabled user (like omkar)

OR give ooo sudo rights (only by root):

sudo usermod -aG sudo ooo

🔚 9. Exit from User Session

Logs out of the current shell session (returns to previous user).

✅ Correct usage.

👑 10. Switch to Root User
su - root
Switches to root account (needs root password).

✅ Correct usage.

🔄 11. Update Package List (as root)
sudo apt update
Refreshes the list of available packages and versions.

✅ Correct usage (when logged in as root or sudoer).

🆕 12. See Upgradable Packages
apt list --upgradable
Shows list of packages that can be upgraded.

✅ Optional but useful.

🔚 13. Exit Root Session
Logs out from root user and returns to previous shell session.

✅ Correct usage.

📝 Summary of Corrections
Command	Issue	Correction
mkdir meals (in /)	❌ Permission denied	sudo mkdir meals
sudo ls (as user ooo)	❌ Not in sudoers	Login as sudoer or add user to sudo group
su - root	✅ OK (requires root password)	-
apt update	✅ OK (if run as root or via sudo)	-

⚠️ Optional: Give Sudo Access to User
sudo usermod -aG sudo ooo
Adds user ooo to sudo group so it can run sudo commands.