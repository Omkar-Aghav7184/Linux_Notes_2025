# 🧠 Linux Command Notes – Shell Configuration, User Switching, and Permissions

This document summarizes only the essential commands (excluding basic navigation like `cd`, `ls`, etc.) with focus on `.bashrc`, `su`, and related actions.

---

## 📝 1. Edit `.bashrc` File

```bash
nano .bashrc
Opens the .bashrc file in the Nano text editor to modify shell settings, aliases, or environment variables.

2. Apply .bashrc Changes
source .bashrc

Reloads .bashrc without restarting the terminal.

Applies changes like aliases or PATH updates.

3. Switch to the Same User Using su
su - omkar
❌ Fails if:

Incorrect password is entered

The user doesn't have login shell access in WSL

Error: Authentication failure

Alternative:
If you're already a sudo-enabled user (like omkar):
sudo -i
Switches to root user or opens a login shell.

📝 Summary Table
Command----> Purpose---->	Correct?------> 	Fix/Alternative
nano .bashrc	Edit shell config	✅	Used to add aliases or env variables
source .bashrc	Reload .bashrc settings	✅	No need to restart terminal
su - omkar	Switch to user omkar	❌	Use correct password or prefer sudo -i
sudo -i	Become root (alternative to su)	✅	Works if you're a sudoer

💡 Tip:
If you want to permanently enable su for a user in WSL:

Set a password for that user:
sudo passwd omkar
Ensure login shell is available in /etc/passwd.

