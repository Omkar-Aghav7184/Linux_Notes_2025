
# Linux Group and User Management - Command Notes

This markdown document explains the commands used in the session along with corrections (if any).

---

## 🗂️ Directory Listing

```bash
ls

Lists all files and directories in the current working directory.

Example output shows files like a b c.mp4, file1.txt, cpTest, etc.

👥 Checking Group Membership
groups
Displays all the groups the current user belongs to.

Output: omkar adm dialout cdrom floppy sudo audio dip video plugdev netdev


groups <username>
Displays groups for the specified user.

Example:
groups omkar
groups root


➕ Adding a New Group
sudo addgroup backendteam
Creates a new group named backendteam.

✅ Correct usage. No issues.

🚫 Adding Non-Existing User to a Group
sudo adduser ooo backendteam
❌ Incorrect if user ooo does not exist.

Error: adduser: The user 'ooo' does not exist.

👤 Creating a New User
sudo adduser ooo
Adds a new user ooo and creates its home directory.

Prompts for password and user info.

✅ Correct usage.

✅ Adding Existing User to Existing Group
sudo adduser ooo backendteam
Adds user ooo to group backendteam.

✅ Correct usage.

🔁 Switching to Another User
su - ooo
Switches to user ooo with a login shell.

✅ Correct usage.

Requires password for user ooo.

🧾 Optional: Suppress Login Message
touch ~/.hushlogin
Prevents the login message from showing up every time user logs in.

Optional step. Not shown in session, but recommended.

✅ Summary
Command	Purpose	Correct?
ls	List files/directories	✅
groups	List current user groups	✅
sudo addgroup backendteam	Create group	✅
sudo adduser ooo backendteam	Add non-existing user to group	❌
sudo adduser ooo	Create user	✅
sudo adduser ooo backendteam	Add existing user to group	✅
su - ooo	Switch user	✅
groups <username>	Check another user's groups	✅

✅ Final User Group Checks
groups
# Output when logged in as ooo: ooo backendteam

groups omkar
# Output: omkar adm dialout cdrom floppy sudo audio dip video plugdev netdev

groups root
# Output: root
