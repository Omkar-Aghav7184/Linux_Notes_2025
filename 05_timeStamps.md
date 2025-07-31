# 🕒 Linux File Timestamps Cheatsheet

Every file in Linux has **three main timestamps**:

| Timestamp | Description |
|----------|-------------|
| **mtime** (Modified Time) | Last time the **file content** was modified |
| **ctime** (Change Time) | Last time the **metadata** (permissions, ownership, name) was changed |
| **atime** (Access Time) | Last time the file was **read or accessed** |

---

## 🔍 Viewing Timestamps with `ls`

### 1. `ls -l` → Shows **mtime**
```bash
ls -l

2. ls -lc → Shows ctime
Shows when the file metadata was changed (renamed, permissions, ownership).

3. ls -lu → Shows atime
Shows the last time the file was accessed (e.g., read using cat, less, etc.).

Use stat to See All Timestamps
stat filename
Example: stat foods.txt

Access: 2025-07-31 23:03:20.000000000 +0530
Modify: 2025-07-31 22:59:10.000000000 +0530
Change: 2025-07-31 23:02:59.000000000 +0530

Access → Last time it was read

Modify → Last time content was changed

Change → Last time metadata was updated

 Quick Summary Table
Action	Updates mtime	Updates ctime	Updates atime
Modify file contents (edit)	✅	✅	❌
Change permissions (chmod)	❌	✅	❌
Rename or move file (mv)	❌	✅	❌
Read file (cat, less, etc)	❌	❌	✅

/***********/
# 📅 Linux Calendar Commands: `cal` and `ncal`

## 1. `cal`
- **Command:** `cal`
- **Description:** Displays the current month's calendar in traditional horizontal format.
- **Example:**
  ```bash
  cal

2. ncal
Command: ncal

Description: Displays the current month's calendar in vertical format (days as rows).

Example:ncal

3. ncal <month> <year>
Command: ncal jan 2025

Description: Shows calendar for January 2025 in vertical format.

Example:
ncal jan 2025

4. ncal <month> <year> -w
Command: ncal july 2025 -w

Description: Adds week numbers at the bottom of the calendar.

Example:
ncal july 2025 -w

5. ncal <month> <year> -wM
Command: ncal july 2025 -wM

Description:

Shows calendar starting from Monday (instead of Sunday).

Includes week numbers.

Example:
ncal july 2025 -wM

6. man ncal
Command: man ncal

Description: Opens the manual page for ncal to view all available options and usage.

Example:

bash
Copy
Edit
man ncal
✅ Note: If ncal doesn't work, install it using:

sudo apt install ncal
