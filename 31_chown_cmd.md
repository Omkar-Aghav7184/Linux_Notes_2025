✅ Users and Groups
Check user groups:

groups
Example:


omkar adm dialout cdrom floppy sudo audio dip video plugdev netdev
Add user to a group (frontendteam):


sudo usermod -aG frontendteam omkar
Verify group membership after re-login or su -:

su - omkar
groups
Output:


omkar adm dialout cdrom floppy sudo ... frontendteam
Switch user:


su - <username>
Example:

su - ooo
✅ Directory Permissions & Ownership
Try renaming a root-owned directory (fails without permission):


mv backend_project/ backend_project_1/
# Output: Permission denied
Grant group write permission to a directory:



sudo chmod g+w backend_project/
Change group ownership to frontendteam:


sudo chown :frontendteam backend_project/
Confirm with ls -l:


ls -ld backend_project/
Example:


drwxrwxr-x 2 root frontendteam ...
✅ File Creation & Access Between Users
User omkar creates file:


nano intro.txt
echo "Omkar ---> TL" > intro.txt
User ooo creates a new file:


nano intro.tx
ooo reads & edits omkar's file because of shared group:


cat intro.txt
# Output: Omkar ---> TL
nano intro.txt
# Appends: ooo---> Senior Software Dev
omkar verifies appended content:


cat intro.txt
# Output:
Omkar ---> TL
ooo---> Senior Software Dev
Changed group of intro.txt to frontendteam:


sudo chown :frontendteam intro.txt
✅ Important Observations
omkar and ooo are both in the frontendteam group.

The directory backend_project/ and file intro.txt are group-writable and owned by frontendteam.

This setup allows controlled collaboration between users in a shared group.

✅ Best Practices
Always use usermod -aG (not -G alone) to append user to a group.

Run su - <user> to reinitialize group changes.

Ensure directories have appropriate permissions:


chmod g+rw <directory>
Set default group for all files in a directory (optional advanced):

sudo chmod g+s backend_project/