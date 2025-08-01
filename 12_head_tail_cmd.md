# 📁 Linux File Viewing & Navigation Commands

A simple log of commands executed with explanations.

---

## 📂 Navigating to Directory

```bash
cd nanoTest
ls
Sample File Used
test.txt
🔼 View Top of File
bash
Copy
Edit
head test.txt
Shows the first 10 lines of the file.

head -n5 test.txt
Shows the first 5 lines of the file.

🔽 View Bottom of File
tail test.txt
Shows the last 10 lines of the file.

tail -n5 test.txt
Shows the last 5 lines of the file.

🔁 Live Monitoring of File (e.g. logs)
tail -f test.txt
Explanation: Continuously shows newly appended lines.
Press Ctrl + C to exit.

📄 Scroll Through File
less test.txt
Explanation: View and scroll forward/backward through file contents.

Press q to quit.

📌 Example Output Snippet (head)

Line 1: This is a sample text file for Linux command testing.
Line 2: You can open this using nano, vi, or any CLI editor.
Line 3: Use `file` command to identify THE file type.
Line 4: Use `cat`, `less`, or `more` to view its contents.
Line 5: This file is purely ASCII text.
📌 Example Output Snippet (tail)

Line 47: File extensions don’t matter to Linux.
Line 48: Content determines file type.
Line 49: This line is here to make it 49.
Line 50: And this one makes it 50!
Line 51: Bonus line! You’re doing great!

✅ Summary Table
Command	Purpose	Notes
head file	View top lines	Default 10 lines
tail file	View bottom lines	Default 10 lines
head -nN file	View first N lines	Replace N with a number
tail -nN file	View last N lines	Replace N with a number
tail -f file	Live monitor file	Useful for logs
less file	Scrollable view	Use arrow keys, q to quit