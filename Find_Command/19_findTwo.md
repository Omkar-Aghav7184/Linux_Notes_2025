# 🕒 `find` Command: Time-Based Search Notes

## ⏳ 1. Modified Time: `-mtime`
Used to find files by last **modification** date.

| Option         | Meaning                                      |
|----------------|----------------------------------------------|
| `-mtime -7`    | Modified **within** last 7 days              |
| `-mtime +7`    | Modified **more than** 7 days ago            |
| `-mtime 7`     | Modified **exactly** 7 days ago              |

📌 Example:
```bash
find . -mtime -7

2. Access Time: -atime
Used to find files by last accessed date.

Option	Meaning
-atime -7	Accessed within last 7 days
-atime +7	Accessed more than 7 days ago
-atime 7	Accessed exactly 7 days ago
find . -atime +7

3. Change Time: -ctime
Used to find files by change in metadata (permissions, owner, etc.)

Option	Meaning
-ctime -7	Changed within last 7 days
-ctime +7	Changed more than 7 days ago
-ctime 7	Changed exactly 7 days ago

📌 Example: find . -ctime -7
🕐 4. Modified Minutes: -mmin
Search by last modified time in minutes.

Option	Meaning
-mmin -700	Modified within last 700 minutes
-mmin +700	Modified more than 700 minutes ago
-mmin 700	Modified exactly 700 minutes ago

📌 Example: find . -mmin -700
🔓 5. Accessed Minutes: -amin
Search by last access time in minutes.

Option	Meaning
-amin -7	Accessed within last 7 minutes
-amin +7	Accessed more than 7 minutes ago
-amin 7	Accessed exactly 7 minutes ago

📌 Example: find . -amin +7
⚙️ 6. Changed Minutes: -cmin
Search by last change time in minutes (permissions, ownership, etc.)

Option	Meaning
-cmin -7	Changed within last 7 minutes
-cmin +7	Changed more than 7 minutes ago
-cmin 7	Changed exactly 7 minutes ago

📌 Example: find . -cmin +7
✅ Summary Table
Flag	Time Type	Unit	Description
-mtime	Last modified	Days	File content change
-atime	Last accessed	Days	When file was last read
-ctime	Metadata changed	Days	Permissions, owner, link count
-mmin	Last modified	Minutes	File content change
-amin	Last accessed	Minutes	When file was last read
-cmin	Metadata changed	Minutes	Permissions, owner, link count